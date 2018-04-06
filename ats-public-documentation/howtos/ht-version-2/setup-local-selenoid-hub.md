# How-to Setup local Selenoid hub #

In this How-to, we show you an example of a simple setup of a Selenoid hub with a Chrome node and a Firefox node on a Linux machine with docker. This will also work on a Windows machine with docker, but the commands and configuration could be slightly different. The official project can be found here: [https://github.com/aerokube/selenoid](https://github.com/aerokube/selenoid) and the official documentation here: [http://aerokube.com/selenoid/latest/](http://aerokube.com/selenoid/latest/).

It is possible to run Selenoid without Docker, but that is outside of the scope of this How-to. Please refer to the official documenation if you would like to achieve this.

## 1. Prerequisites ##

- Some basic docker and docker-compose knowledge.
- A machine with the latest versions of **docker** and **docker-compose** installed.
- Your machine should allow connections from ATS on port 4444.



## 2. Install your hub and nodes with Docker-Compose ##

- Create a folder or directory to place your docker-compose.yml and browser.json files.

In our example **/docker**

- Create a folder or directory to place your video files

In our example **/docker/video**

- Create a browser.json in your folder/directory (/docker)

```
{
        "firefox": {
                "default": "58.0",
                "versions": {
                        "58.0": {
                                "image": "selenoid/firefox:58.0",
                                "port": "4444",
                                "path": "/wd/hub",
                                "tmpfs": {"/tmp":"size=512m"}
                        }
                }
        },
        "chrome": {
                "default": "65.0",
                "versions": {
                        "65.0": {
                                "image": "selenoid/chrome:65.0",
                                "port": "4444",
                                "tmpfs": {"/tmp":"size=512m"},
                                "shmSize" : 1073741824
                        }
                }
        }
}
```

- Create a docker-compose.yml in your folder/directory (/docker)

```
version: '3'
services:
  selenoid:
    network_mode: bridge
    image: aerokube/selenoid
    volumes:
      - "/docker:/etc/selenoid"
      - "/var/run/docker.sock:/var/run/docker.sock"
      - "/docker/video:/opt/selenoid/video"
    environment:
      - OVERRIDE_VIDEO_OUTPUT_DIR=/opt/selenium/video
      - TZ=Europe/Amsterdam
    command: ["-conf", "/etc/selenoid/browsers.json", "-video-output-dir", "/opt/selenoid/video"]
    ports:
      - "4444:4444"
```

- Open a console and give the following commands to pull the images first:

```
sudo docker pull selenoid/chrome:65.0
sudo docker pull selenoid/firefox:58.0
sudo docker pull selenoid/video-recorder
sudo docker pull aerokube/selenoid
```

- Open a console and give the following command from the folder/directory where your docker-compose.yml is placed:

```
sudo docker-compose up -d

Starting docker_selenoid_1 ... done
```

- After it's done starting, you can check the status

```
sudo docker-compose ps
      Name                     Command               State           Ports         
-----------------------------------------------------------------------------------
docker_selenoid_1   /usr/bin/selenoid -conf /e ...   Up      0.0.0.0:4444->4444/tcp
```

- To check the status of the hub

```
curl -s http://localhost:4444/status

{"total":5,"used":0,"queued":0,"pending":0,"browsers":{"chrome":{"65.0":{}},"firefox":{"58.0":{}}}}
```

## 3. Start Testing ##

You can start testing by sending your test script to: [http://yourmachinenameorIP:4444/wd/hub](http://localhost:4444/wd/hub).  Make sure it is reachable from the outside!

