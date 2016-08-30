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


The server will display the ip and port it is running on (example: 192.168.0.123:3000). You will need this later to connect.

**If you run into any issues, scroll down to the Troubleshooting section**

# Setting up Client

Download and install [Genymotion](https://www.genymotion.com/download/)

**You can install APKs in Genymotion simply by dragging and dropping them to your device screen.**

#### Prepackaged Device
1. Download prepackaged device [Download coming soon]
2. Create a new device in Genymotion (Google Nexus 6P - 6.0.0 - API 23)
3. Find your "Deployed Devices" directory and replace your device folder (example: Google Nexus 6P - 6.0.0 - API 23 - 1440x2560) with the one you downloaded
  * OS X Location: ~/.Genymobile/Genymotion/deployed/
4. Open up the PokemonGo Xposed Module app and change "set custom endpoint" to your server ip:port (example: 192.168.0.123:3000) 

#### Manual Setup
1. Create a new device in Genymotion
2. Follow [this tutorial](http://forum.xda-developers.com/android/general/guide-genymotion-play-store-supersu-t3396840) to install ARM Translation, GApps, and then Xposed on your device.
3. Enable the PokemonGo Exposed Module within the Xposed Framework app and restart device. 
4. Download and install the [PokemonGo Xposed Module](https://github.com/rastapasta/pokemon-go-xposed/releases/download/v2.2/PokemonGoXposed.apk)
5. Open up the PokemonGo Xposed Module app and change "set custom endpoint" to your server ip:port (example: 192.168.0.123:3000) and enable custom url.
6. Switch Enable Custom Endpoint to on.




# Troubleshooting

### Node related errors
First try and remove your current node_modules and reinstall your modules with ```npm install```. Make sure you have node 6.4 or higher with ```npm -v```

If you're still running into errors, you can try and download a prepackaged node_modules directory to replace your current one. 
* [Node Modules for Windows](https://mega.nz/#!SUUDXBZQ)
* [Node Modules for OS X](https://mega.nz/#!DNUTzB5K)

### Missing game_master or cannot download game assets
If you get an error about game_master or are unable to download the game assets, you can download the data/ directory [here](https://mega.nz/#!uNUWQCqS).

### Issues logging in from game
Make sure the account you are trying to login with is NOT banned and you have logged into the Niantic PokemonGo servers at least once with your account. 

### Protobuf Issues
**You must compile install protobuf to your machine.***

### Cant login to web api
The default login is root and the default password is 13377. You can change the password by editing the file ```.save``` in your main server directory. (This file might be hidden)

### Pokemon not spawning
In order to spawn pokemon, you can type into the console ```/spawn usernamehere POKEMONNAME 10```. You then need to restart your PokemonGo app (not server) to see the spawned pokemon.
