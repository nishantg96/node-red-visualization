# Node-Red Visualization Demo
This is a demonstration of different visualization components all connected together on the same network and running on node-red. 

----
There are 4 main parts of this project:
   1. Visualization on an external notification device
   2. Visualization on LED strip
   3. Using language translator and Text-to-Speech
   4.  Object classification
----
For using the language translator, Text-to-Speech and Object classification we use the [Watson cloud services](https://cloud.ibm.com/).

## Quick Start
   1. Register on [Watson cloud services](https://cloud.ibm.com/login).
   2. Install the latest version of NodeJS and node-red.

### Installing NodeJS

#### Windows

>Install using the package file. [Download Windows Installer](http://nodejs.org/#download).


#### Ubuntu
##### **1. Remove the old PPA if it exists**
   
This step is only required if you previously used Chris Lea's Node.js PPA.

```sh
sudo add-apt-repository -y -r ppa:chris-lea/node.js
sudo rm -f /etc/apt/sources.list.d/chris-lea-node_js-*.list
sudo rm -f /etc/apt/sources.list.d/chris-lea-node_js-*.list.save
```

##### **2. Add the NodeSource package signing key**

```sh
curl -fsSL https://deb.nodesource.com/gpgkey/nodesource.gpg.key | sudo apt-key add -
                            OR
wget --quiet -O - https://deb.nodesource.com/gpgkey/nodesource.gpg.key | sudo apt-key add -
```
##### **3. Add the desired NodeSource repository**

```sh
VERSION=node_15.x
DISTRO="$(lsb_release -s -c)"
echo "deb https://deb.nodesource.com/$VERSION $DISTRO main" | sudo tee /etc/apt/sources.list.d/nodesource.list
echo "deb-src https://deb.nodesource.com/$VERSION $DISTRO main" | sudo tee -a /etc/apt/sources.list.d/nodesource.list
```

##### **4. Update package lists and install Node.js**

```sh
sudo apt-get update
sudo apt-get install nodejs
```

### Installing Node-red

#### Windows

Check if NodeJS and NPM are installed properly and up-to-date using:

```sh
node --version; npm --version   on powershell
node --version && npm --version    on CMD
```
If everything is installed properly, install node-red using:

```sh
npm install -g --unsafe-perm node-red
```

#### Ubuntu

```sh
#After installing NodeJS and NPM
sudo npm install -g --unsafe-perm node-red
```

### NodeJS and Node-red on Raspberry Pi

Installing and updating NodeJS and Node-red on Raspberry Pi is very easy. Running the following command will download/insstall/update NodeJS and Node-red.This script will work on any Debian-based operating system. You may need to run sudo apt install build-essential git first to ensure npm is able to build any binary modules it needs to install. 

```sh
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)

```
### Adding Watson API to node-red

The watson node-red package can be installed either by commandline or by adding it from node-red pallete. To install it from the node-red pallete:

>Settings -> Manage pallete -> Install tab -> search for "node-red-node-watson" -> install

The Watson package with all the required nodes will be installed. 

To install it from commandline, use the command:

```sh
npm install node-red-node-watson
```
