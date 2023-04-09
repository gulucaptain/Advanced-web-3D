# Advanced-web-3D

Welcome to the class of Advanced Web Techonology.

## Lab2: Create an online multi-player game. 

<img width="1283" alt="image" src="https://user-images.githubusercontent.com/35996667/230751420-5014fd0a-d0d5-428a-bac3-3282c28fc67c.png">

In this game, you can move around the map, invite your friends join in, and communicate with them. An demo can be visited at: http://124.223.224.204:3000. (Clikc your friend, you can talk to him with the Talking Bar.)

You can achieve this game with NodeJS, Socket.io, and Three.js. The following steps will help you to complete your lab.

### STEPs

1. Download the source code from: https://github.com/PMLS3/3D-multi-player. Also thanks for the great developer. 
2. [Important] You can learn related course from bilibili: https://www.bilibili.com/video/BV1th411J7zo/?spm_id_from=333.337.search-card.all.click&vd_source=1068ea6e2b9d5d54342d2f2dfc0faa0f.
3. Installing NodeJS in cloud server.
* Download node package at https://nodejs.org/en/download/. Choose the Linux binaries (x64) version that the suffix of the file ends with '.xz'.
* Upload the file to the /usr/local/ path.
* Unzip files with: tar -xvf node-vxx.xx.xx-linux-x64.tar.xz
* Rename the unzipped file: mv node-vxx.xx.xx-linux-x64 node
* Build the soft connection:
   * vi /etc/profile, then add the following contents:
   * export NODE_HOME=~/usr/local/node
   * export PATH=$NODE_HOME/bin:$PATH
* Check the node and npm: node -v; npm -v.
4. Install the dependency. To run the project, the related dependencies should be installed, including express and socket.io.
* cd ~/3D-multi-player-main/nodeapps/blockland
* Remove old files: rm -rf package-lock.json; rm -rf package.json.
* Initialization: npm init. Just select the default option.
* Install express package: npm install express@4.15.2 --save
* Install socket.io: npm install socket.io@2.2.0 --save
5. Run the project: /3D-multi-player-main/nodeapps/blockland$ node app.js
* The default port is 2002, you can change the port in app.js, line 50 and 51.
6. Forever keep the node project online. Because the node server will be offline when remote loss connection. To keep the project online, the forever package will help us.
* Install the forever: npm install forever -g
* Run app.js with forever: forever start app.js

### Congratulation: your own multi-player game is online!
