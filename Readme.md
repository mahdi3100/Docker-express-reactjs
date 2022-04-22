# Crypto Widget  

 
This widget will be used to display several currency exchanges rates and it will allow the user to exchange USD for
Crypto . The application consists of a React front-end client and a Node back-end service (Express.js) and a docker to run it.
 
## Features

Get and update rate for each given time period (by default 30s) with random cryptocurrency (BTC, XRP, ETH) to (USD, EUR, GBP) and display result in history table using websocket.

User can store/save The exchange from (BTC , XRP , ETH) to (USD , EUR , GBP) and show the result in history's table .

User can sort all the columns of history's table.

User can filter history by one giving Date. using react-table

User can filter history between Dates. using sql request

All data is stored in the database.


 
## Requirements 

The app use Docker compose .

##Start the application

To start the app : 

```bach 
cd /path/to/docker-compose.yaml
docker-compose build
docker-compose up
```

In case of port 3306 issue caused by mysql in docker , you have to stop your local mysql   
```bach 
/etc/init.d/mysql stop
```

Then go to browser and check **http://127.0.0.1:3000**

## Tree

Tree for the app "red"

```bach 

├── client
│   ├── Dockerfile
│   ├── package.json
│   ├── package-lock.json
│   ├── public
│   │   ├── favicon.ico
│   │   ├── index.html
│   │   ├── logo192.png
│   │   ├── logo512.png
│   │   ├── manifest.json
│   │   └── robots.txt
│   ├── README.md
│   ├── src
│   │   ├── all.min.css
│   │   ├── App.css
│   │   ├── App.js
│   │   ├── App.test.js
│   │   ├── ExchangeContext.js
│   │   ├── index.css
│   │   ├── index.js
│   │   ├── logo.svg
│   │   ├── reportWebVitals.js
│   │   ├── setupTests.js
│   │   ├── Table.js
│   │   └── Toolbar.js
│   └── webfonts
├── database
│   └── red.sql
├── docker-compose.yml
├── Readme.md
└── server
    ├── app.js
    ├── Dockerfile
    ├── package.json
    ├── package-lock.json
    └── routes
        ├── convert.js
        ├── db.js
        ├── history.js
        └── rate.js

```



## Utility of files 

**Client/src/Toolbar.js:** It's the component of Toolbar 

**Client/src/Table.js:** It's the component of History 

**Client/src/App.js** Gather Components

**Client/src/index.js** Main react file for client

**Client/public/index.html** The index of view , Public html file.

**server/app.js** Main server file for express , Api file
		

## DataBase

To edit sql file or database file , you have to browse to phpmyadmin which has been already installed with docker , go to http://127.0.0.1:8081   .  

Login: 
username : root
password : ok

browse to database name "red", voila



## Notes

The deisign of History Component does not fit on mobile (not yet).
The app is not in build state - production. 

