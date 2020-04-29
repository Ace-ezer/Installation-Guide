
## Debian and Ubuntu based distributions

### Installation instructions

#### Prerequisites

> This guide assumes that you are using Ubuntu 18.04. Before you begin, you should have a non-root user account with sudo privileges set up on your system. You can learn how to do this by following the initial server setup tutorial for Ubuntu 18.04.
Installing the Distro-Stable Version for Ubuntu

>Ubuntu 18.04 contains a version of Node.js in its default repositories that can be used to provide a consistent experience across multiple systems. At the time of writing, the version in the repositories is 8.10.0. This will not be the latest version, but it should be stable and sufficient for quick experimentation with the language.

To get this version, you can use the apt package manager. Refresh your local package index by typing:
```
    sudo apt update
```
Install Node.js from the repositories:
```
    sudo apt install nodejs
```
If the package in the repositories suits your needs, this is all you need to do to get set up with Node.js. In most cases, you’ll also want to also install npm, the Node.js package manager. You can do this by typing:
```
    sudo apt install npm
```
This will allow you to install modules and packages to use with Node.js.

Because of a conflict with another package, the executable from the Ubuntu repositories is called nodejs instead of node. Keep this in mind as you are running software.

To check which version of Node.js you have installed after these initial steps, type:
```
    nodejs -v
```

## Upgrading to current stable version

```
sudo npm cache clean -f
sudo npm install -g n
sudo n stable
```

## Version check
* NodeJs
```
node -v
```
* NPM
```
npm -v
```