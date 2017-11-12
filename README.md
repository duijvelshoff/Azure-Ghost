# Ghost on Azure App Service

This is my fork of [Ghost 1.0 by Chadly](https://github.com/chadly/ghost) with changes to run on Azure **Web App + MySQL** Service. [Read here the original documentation.](https://www.chadly.net/ghost-on-azure/)

## Installation

After the deploy based on the original documentation simply run: `bash initialize.sh`

## Changes

* Add `initialize.sh` & `init/` - Initalization of the Ghost Database on MySQL.
* Removed `db.js` - Not used anymore + in-app MySQL results in an error.
* Removed `config.development.json` & `config.production.json` - Not used anymore; `initialize.sh` generates `config.production.json`.