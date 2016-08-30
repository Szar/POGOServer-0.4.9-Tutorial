# Prerequisites
* Node 6.4 or higher
  * [Download for Windows](https://nodejs.org/dist/v6.4.0/node-v6.4.0-x64.msi)
  * [Download for OS X](https://nodejs.org/dist/v6.4.0/node-v6.4.0.pkg)
  * [Download for Linux](https://nodejs.org/dist/v6.4.0/node-v6.4.0-linux-x64.tar.xz)
  * [Download Source Code](https://nodejs.org/dist/v6.4.0/node-v6.4.0.tar.gz)
* Protobuf 3.0
  * [Download the source code](https://github.com/google/protobuf/releases/download/v3.0.0/protobuf-cpp-3.0.0.zip) and compile by following [these instructions](https://github.com/google/protobuf/blob/master/src/README.md) for your OS
* Git
  * [Download for Windows](https://git-scm.com/download/win)
  * [Download for OS X](https://git-scm.com/download/mac)
  * [Download for Linux](https://git-scm.com/download/linux)
* MySQL Database
  * [MySQL Community Server](http://dev.mysql.com/downloads/mysql/)
  * OR get a free database from any service like https://www.db4free.net/



# Setting Up 0.4.9 Server

1. Download server files: https://mega.nz/#!nQFiiLCb
2. Edit cfg.js lines 39 to 42
```
  MYSQL_HOST_IP: "MYSQL HOST HERE",
  MYSQL_DB_NAME: "DATABASE NAME HERE",
  MYSQL_USERNAME: "USERNAME HERE",
  MYSQL_PASSWORD: "USER PASSWORD HERE",
```
3. Run server 
  * Windows: Double click run-windows.bat
  * Linux/OS X: Run in terminal ```sh run-linux.sh```

**If you run into any issues, scroll down to the Troubleshooting section**

# Setting up Client

1. Download and install [Genymotion](https://www.genymotion.com/download/)
2. 





# Troubleshooting

#### Node related errors
First try and remove your current node_modules and reinstall your modules with ```npm install```. Make sure you have node 6.4 or higher with ```npm -v```

If you're still running into errors, you can try and download a prepackaged node_modules directory to replace your current one. 
* [Node Modules for Windows](https://mega.nz/#!SUUDXBZQ)
* [Node Modules for OS X](https://mega.nz/#!DNUTzB5K)

#### Missing game_master or cannot download game assets
If you get an error about game_master or are unable to download the game assets, you can download the data/ directory [here](https://mega.nz/#!uNUWQCqS).

