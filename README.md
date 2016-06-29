## jsf-kss

This is example repository to make jsf
Please don't use for commercial


## HOW TO SETTING

- $ cd jsf-server && npm install
- $ DEBUG=jsf-server:* npm start or $ npm start
(node_modules delete & npm install)


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

### PRE-REQUISITE

- $ npm install -g express
- $ npm install -g express-generator
- $ express jsf-server