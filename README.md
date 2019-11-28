# NodeBB OAuth SSO for rehaupro.com

This is the SSO plugin for the nodebb installation of rehaupro.com.
This plugin is based on the skeleton of Julian Lam.

The original source code can be found here: https://github.com/julianlam/nodebb-plugin-sso-oauth


# Build 

separate build not required

build performed during installation to nodebb forum

# Install on nodebb forum

## Prerequisites
nodebb installed in '/home/portal/nodebb' from user portal

## Installation
`su - portal`
`git clone https://xxxx/nodebb-plugin-sso-oauth-rehau.git`
`cd nodebb-plugin-sso-oauth-rehau`
`sudo npm link`
`cd ~/nodebb`
`./nodebb stop`
`cd node_modules`
`npm link nodebb-plugin-sso-oauth-rehau`

`cd /home/portal`
`git clone https://xxxx/nodebb-plugin-sso-oauth-rehau.git nodebb-plugin-sso-oauth-rehau-mont`
`cd nodebb-plugin-sso-oauth-rehau-mont`
`git checkout montage`
`sudo npm link`
`cd ~/nodebb/node_modules`
`npm link nodebb-plugin-sso-oauth-rehau-mont`
`cd ~/nodebb`
`./nodebb build tpl`
`./nodebb start`
