# Setting up a local Selenium Solution #

In this How-to we will describe a few possible local Selenium solutions and a small example for each how to set it up. Before we start keep the following points in mind:

- These solutions are all under heavy development and new versions are released on a regular base. These are just examples and we recommend using the official documentation.
- ATS 2 is running in the Mendix cloud. When running a local Selenium solution, ATS should be able to communicate with the machine on port 4444. In most cases this means your network department has to arrange something to make this work.
- **Security warning!!!:** By default, non of the solutions use SSL or any form of authentication. You might, for example, want to use a webserver as a frontend to make SSL and authentication possible. This is not covered in the How-to's.
- Docker Selenium and Selenoid are two opensource projects based on Selenium, we cover in this How-to. There are many more, but we limit us to these two. 
- Support for open source software could be limited or slower.

## 1. Setup Local Selenium hub (SeleniumHQ) ##

- Official website ([https://www.seleniumhq.org/](https://www.seleniumhq.org/))
- How-to set it up link
- Live-view only on the machine where Selenium is installed
- No (out-of-the-box) video recording

## 2. Setup Local Docker Selenium hub (Docker Selenium) ##

- Official github page ([https://github.com/SeleniumHQ/docker-selenium](https://github.com/SeleniumHQ/docker-selenium))
- How to set it up link
- Browsers run in Linux containers
- Live-view possible with debug images and VNC (viewer)
- No (out-of-the-box) video recording

## 3. Setup Local Selenoid hub (Aerokube) ##

- Selenoid is a powerful Go implementation of original Selenium hub code. It is using Docker to launch browsers.
- Official website ([http://aerokube.com/](http://aerokube.com/))
- While ATS works fine with Selenoid (since it's based on the official Selenium code) and it even supports parallel testing on the Selenoid hub. We can't guarantee it will always be supported in the future.
- How-to set it up link
- Browsers run in Linux containers
- Live-view with a seperated to be installed portal. Works with debug browser images and vnc.
- It also has a out-of-the box video recording option

## 4. Why you would prefer a SaaS-solution for Selenium (like Browserstack or Saucelabs) ##

- Active support team
- Secures your connections
- Out-of-the box video recording and live-view in your personal portal
- Always the latest browsers and drivers
- Out-of-the box tunneling solution for local testing
- You can easily test on different OS's and browser versions in any combination you like
- No need to maintain your own servers (OS patches, software updates, network, etc.)
- You can easily scale up