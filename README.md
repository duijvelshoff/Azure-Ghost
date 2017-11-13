# Ghost on Azure App Service

This is my fork of [Ghost 1.0 by Chadly](https://github.com/chadly/ghost) with the needed changes to run on Azure **Web App + MySQL** Service and a few stuff more.

## Prerequisites

- This deployment uses the [Let's Encrypt Extension](https://github.com/sjkp/letsencrypt-siteextension/). Before deployig Ghost, you need to configure a Service Pincipal documented [here](https://github.com/sjkp/letsencrypt-siteextension/wiki/How-to-install#create-a-service-principal). - *Do this untill "Configure the Site Extension".*
- Create a sub-domain `blog`  with a `CNAME`-record to `deployghostblog.azurewebsites.net.` (values based on defaultValue in: **azuredeploy.json**). - *If you want to use a normal domain, follow the usual steps and remove the Web App.*

## Installation

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](http://surlt.xyz/ghost-installation)

*For the parameters requested on the "Setup" page of the Azure deploy, use [this chapter](https://github.com/sjkp/letsencrypt-siteextension/wiki/How-to-install#configure-the-site-extension) to guide you.*