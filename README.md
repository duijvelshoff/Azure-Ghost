# Ghost on Azure App Service

This is my fork of [Ghost 1.0 by Chadly](https://github.com/chadly/ghost) with changes to run on Azure **Web App + MySQL** Service. [Read here the original documentation.](https://www.chadly.net/ghost-on-azure/)

## Installation

After the GitHub deploy in the original documentation, take the following steps:
1. App Service > Custom Domain - Add {domainname}
2. App Service > Application Config - App Settings: url = https://{domainname}/
3. Use the [following documentation](https://github.com/sjkp/letsencrypt-siteextension/wiki/How-to-install) for the Let's Encrypt extension.
4. App Service > Console - Run: `bash initialize.sh`

Done!

## Changes

* Add `initialize.sh` & `init/` - Initalization of the Ghost Database on MySQL.
* Removed `db.js` - Not used anymore + in-app MySQL results in an error.
* Removed `config.development.json` & `config.production.json` - Not used anymore; `initialize.sh` generates `config.production.json`.
* Modified `web.config` - Added the needed route for Let's Encrypt.