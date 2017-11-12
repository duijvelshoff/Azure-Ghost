# Ghost on Azure App Service

This is my fork of [Ghost 1.0 by Chadly](https://github.com/chadly/ghost) with changes to run on Azure **Web App + MySQL** Service.

## Prerequisites

This deployment uses the [Let's Encrypt Extension](https://github.com/sjkp/letsencrypt-siteextension/). Before deployig Ghost, you need to configure a Service Pincipal documented [here](https://github.com/sjkp/letsencrypt-siteextension/wiki/How-to-install#create-a-service-principal). 

*Do this untill "Configure the Site Extension".*

## Installation

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](http://surlt.xyz/ghost-installation)

*For the parameters requested on the "Setup" page of the Azure deploy, use [this chapter](https://github.com/sjkp/letsencrypt-siteextension/wiki/How-to-install#configure-the-site-extension) to guide you.*

## Changes

* Add `initialize.sh` & `init/` - Initalization of the Ghost Database on MySQL.
* Removed `db.js` - Not used anymore + in-app MySQL results in an error.
* Removed `config.development.json` & `config.production.json` - Not used anymore; `initialize.sh` generates `config.production.json`.
* Modified `web.config` - Added the needed route for Let's Encrypt.