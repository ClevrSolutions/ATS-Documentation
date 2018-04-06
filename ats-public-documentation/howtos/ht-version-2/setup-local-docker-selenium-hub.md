# How-to Setup local Docker Selenium hub #

In this How-to, we show you an example of a simple setup of a Docker Selenium hub with a Chrome node and a Firefox node on a Linux machine. This will also work on a Windows machine with docker, but the commands and configuration could be slightly different. The official project can be found here: [https://github.com/SeleniumHQ/docker-selenium](https://github.com/SeleniumHQ/docker-selenium)

## 1. Prerequisites ##

- Some basic docker and docker-compose knowledge
- A machine with **docker** and **docker-compose** installed
- Your machine should allow connections from ATS on port 4444.
- Since version 2.6, ATS uses the Selenium 3.8.1 API. That's why we recommend using this version of Selenium for the docker images as well.


## 2. Install your hub and nodes with Docker-Compose ##

- Create a folder or directory to place your docker-compose file
- Create a docker-compose.yml in your folder/directory

docker-compose.yml:

    hub: 
     image: selenium/hub:3.8.1
     environment:
       - TZ=Europe/Amsterdam
       - GRID_TIMEOUT=90
     ports:
       - 4444:4444
    
    firefox:
     image: selenium/node-firefox:3.8.1
     links:
       - hub:hub
     environment:
       - TZ=Europe/Amsterdam
       - SCREEN_WIDTH=1600
       - SCREEN_HEIGHT=900
    
    chrome:
     image: selenium/node-chrome:3.8.1
     links:
       - hub:hub
     environment:
       - TZ=Europe/Amsterdam
       - SCREEN_WIDTH=1600
       - SCREEN_HEIGHT=900
     volumes:
       - /dev/shm:/dev/shm
     privileged: true

- Open a console and give the following command from the folder/directory where your docker-compose.yml is placed:

```
sudo docker-compose up -d
```

The first time it will start pulling the images from the Docker hub.

- After it's done starting, you can check the status

```
sudo docker-compose ps
      Name                 Command           State           Ports         
---------------------------------------------------------------------------
docker_chrome_1    /opt/bin/entry_point.sh   Up                            
docker_firefox_1   /opt/bin/entry_point.sh   Up                            
docker_hub_1       /opt/bin/entry_point.sh   Up      0.0.0.0:4444->4444/tcp
```

- You can check if it works: [http://localhost:4444/grid/console](http://localhost:4444/grid/console)

## 3. Optional: Scale your nodes ##

Each node has one browser if you need more nodes of a certain browser, you can easily scale with docker-compose. For example, if you want 3 chrome browsers, because you want to run tests parallel:

```
sudo docker-compose up -d --scale chrome=3
docker_hub_1 is up-to-date
Starting docker_chrome_1 ... 
Starting docker_chrome_1 ... done
Creating docker_chrome_2 ... done
Creating docker_chrome_3 ... done

sudo docker-compose ps
      Name                 Command           State           Ports         
---------------------------------------------------------------------------
docker_chrome_1    /opt/bin/entry_point.sh   Up                            
docker_chrome_2    /opt/bin/entry_point.sh   Up                            
docker_chrome_3    /opt/bin/entry_point.sh   Up                            
docker_firefox_1   /opt/bin/entry_point.sh   Up                            
docker_hub_1       /opt/bin/entry_point.sh   Up      0.0.0.0:4444->4444/tcp
```

**Note:** the hub default only accepts a maximum 5 sessions to run parallel at a time (although you configure more, see the official documentation).

## 4. Optional: Installing a hub with "Live-view" through VNC ##

If you want to watch your test case being played live for debugging purpose you can use the following docker-compose.yml:

    hub: 
     image: selenium/hub:3.8.1
     environment:
       - TZ=Europe/Amsterdam
       - GRID_TIMEOUT=90
     ports:
       - 4444:4444
    
    firefox:
     image: selenium/node-firefox-debug:3.8.1
     links:
       - hub:hub
     environment:
       - TZ=Europe/Amsterdam
       - SCREEN_WIDTH=1600
       - SCREEN_HEIGHT=900
     ports:
       - 5901:5900
    
    chrome:
     image: selenium/node-chrome-debug:3.8.1
     links:
       - hub:hub
     environment:
       - TZ=Europe/Amsterdam
       - SCREEN_WIDTH=1600
       - SCREEN_HEIGHT=900
     ports:
       - 5900:5900
     volumes:
       - /dev/shm:/dev/shm
     privileged: true

- Notice that you are using debug versions of the browser images.
- You will need a vnc-client like Tigervnc ,VNC Viewer for Google Chrome or any other favorite client of your choice.
- For Chrome you use as the address: localhost:5900 (or machinename/ip:5900) with password "secret"
- For Firefox you use: localhost:5901 (or machinename/ip:5901) with password "secret"
- You cannot scale using this configuration
- Be aware that vnc is not a very secure protocol, you might not want to open this port for the world
