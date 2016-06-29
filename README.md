## jsf-kss

This is example repository to make jsf
Please don't use for commercial


## HOW TO SETTING

- $ cd jsf-server && npm install
- $ DEBUG=jsf-server:* npm start or $ npm start
(node_modules delete & npm install)


## Running Background Daemon

### Using Forever npm module

- $ npm install -g forever

#### forever execute example

> Start app 
- $ forever --minUptime 5 --spinSleepTime 5 start app.js

> Stop app
- $ forever list
- $ forever stop 0 (it will be changed.. see the result of list command)

## Mongo-DB Install

- $ sudo apt-get install -y mongodb-org

- $ mkdir data
- $ echo 'mongod --bind_ip=$IP --dbpath=data --nojournal --rest "$@"' > mongod
- $ chmod a+x mongod

- $ ./mongod

- --dbpath=data - Because it defaults to /var/db (which isn't accessible)
- --nojournal - Because mongodb usually pre-allocates 2 GB journal file (which exceeds Cloud9 disk space quota)
- --bind_ip=$IP - Because you can't bind to 0.0.0.0
- --rest - Runs on default port 28017

## MySQL Install

### using C9
- $ mysql-ctl install
- $ mysql-ctl cli
 
### using Linux Machine
- $ sudo apt-get install mysql-server

## Switch DB Protocol (MongoDB -> MySQL) 
- $ mv ./jsf-server/app.js ./jsf-server/app_mongodb.js && mv ./jsf-server/app_mysql.js ./jsf-server/app.js



## PRE-REQUISITE

- $ npm install -g express
- $ npm install -g express-generator
- $ express jsf-server