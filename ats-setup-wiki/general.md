ATS runs on top of Mendix 6. See Mendix for their [system requirements](https://docs.mendix.com/refguide6/System+Requirements).

# Component Overview ATS
An ATS implementation consists of:
*  Mendix Business Server running in Java JVM
*  Mendix deployment folder used by the Mendix Server
*  Database
*  One or more Selenium server instances (alternatively a Selenium provider
   like Browserstack or Saucelabs)
*  Optionally a web server to serve static content
*  Data within ATS

The ATS architecture:
![ATS architecture](ATS_architecture.png "ATS architecture")

# Compatibility
Please distinguish between compatiblity for running/using ATS and the
compatibility for testing other applications with ATS.

This chapter describes how to set up ATS.

# Hardware requirements / Hardware sizing
## Mendix Business Server
A recent CPU (minimal dual core, minimal 2 GHz), 4 GB of memory and a
free disk space of 10 GB is recommended.

## Database Server
A recent CPU (minimal dual core, minimal 2 GHz), 4 GB of memory and a
free disk space of 20 GB is recommended.

## Selenium Server(s)

|   | Standalone server | Grid hub | Grid Node |
|---|---|---|---|
| Minimal | Recent CPU, 1GHz 2GB RAM | Recent CPU, 1GHz 2GB RAM | Recent CPU, 1GHz 2GB RAM |
| In addition per browser instance* | 1 Core, 1GHz 500MB RAM | 200MHz 200MB RAM | 1 Core, 1GHz 500MB RAM |

_*_ Highly depends on the browser and on the application that is tested. The defined resources are for medium sized applications.

# Software requirements
This chapter describes the software requirements for running ATS.

## Operating System
See [official documentation](https://docs.mendix.com/refguide6/System+Requirements#operating-system). ATS itself has no requirements regarding the operating system.

## Java
See [official documentation](https://docs.mendix.com/refguide6/System+Requirements#java). ATS itself has no requirements regarding Java.

## Mendix Business Server
ATS requires Mendix business server, version 6.8.0.

## Database
See [official documentation](https://docs.mendix.com/refguide6/System+Requirements#database-server). ATS itself has no requirements regarding the database.

## Selenium
Only the selenium server version that is delivered as part ot the ATS installation is supported.

| ATS Version | Supported Selenium version | Download | Required Java version |
|---|---|---|---|
| 1.8 | 2.53.0 | [Download here](http://selenium-release.storage.googleapis.com/2.53/selenium-server-standalone-2.53.0.jar) | JRE 7 |

## Chromedriver
Only the Chromedriver version that is delivered as part of the ATS installation is supported.

| ATS Version | Supported Chromedriver version | Download |
|-------------|--------------------------------|----------|
| 1.8 | 2.23 | [Download here](http://chromedriver.storage.googleapis.com/index.html?path=2.23/) |

## Browsers
The following browsers are supported to operate ATS (on their supported OS):
* Firefox 17 (ESR) or higher
* Google Chrome 22 or higher
* Internet Explorer 11
