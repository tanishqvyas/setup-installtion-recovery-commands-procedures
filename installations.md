# My installations for a new OS

## Pre-requisites

### curl
```bash
sudo snap install curl
```

### net-tools
```bash
sudo apt install net-tools
```

### nmap
```bash
sudo apt install nmap
```

### netdiscover

```bash
sudo apt install netdiscover
```


## Chrome Web Browser

* Install the `google-chrome-stable_current_amd64.deb` file from the official website.
* Change the current directory to the one where the file is downloaded.
* Execute the following command

```bash
sudo dpkg -i <filename>.deb
```

## GIT

```bash
sudo apt update
```

```bash
sudo apt install git
```

```bash
git --version
```

Additionally refer to [this link](https://stackoverflow.com/questions/68775869/support-for-password-authentication-was-removed-please-use-a-personal-access-to) when facing `Support for password authentication was removed. Please use a personal access token instead` issue while setting up git.

## Setting up SSH for Github

[Reference for Github](https://medium.com/featurepreneur/setting-up-ssh-key-with-github-for-ubuntu-cd8f2fabf25b)




## Node & NPM (Node Package Manager)

Following the Commands stated on the [Digital Ocean | Node installation on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04)

```bash
sudo apt update
```

```bash
sudo apt install nodejs npm
```

```bash
node -v
```

```bash
npm --version
```

To be able to compile native addons from npm you’ll need to install the development tools

```bash
sudo apt install build-essential
```

## Python3 & PIP


### Step 1 : Setting up Python3

Source : [How To Install Python 3 and Set Up a Programming Environment on an Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-programming-environment-on-an-ubuntu-20-04-server)

Ubuntu 20.04 and other versions of Debian Linux ship with Python 3 pre-installed. To make sure that our versions are up-to-date, let’s update and upgrade the system with the apt command to work with Ubuntu’s Advanced Packaging Tool

```bash
sudo apt update
```

```bash
sudo apt -y upgrade
```

The `-y` flag will confirm that we are agreeing for all items to be installed, but depending on your version of Linux, you may need to confirm additional prompts as your system updates and upgrades.

Once the process is complete, we can check the version of Python 3 that is installed in the system by typing:

```bash
python3 -V
```

To manage software packages for Python, let’s install pip, a tool that will install and manage programming packages we may want to use in our development projects.

```bash
sudo apt install -y python3-pip
```

```bash
pip3 --version
```

Python packages can be installed by typing:

```bash
pip3 install <package-name>
```

There are a few more packages and development tools to install to ensure that we have a robust setup for our programming environment:

```bash
sudo apt install -y build-essential libssl-dev libffi-dev python3-dev
```


### Step 2 : Setting Up a Virtual Environment

```bash
sudo apt install -y python3-venv
```


## Sublime Text

```bash
sudo apt update
```

```bash
sudo apt install dirmngr gnupg apt-transport-https ca-certificates software-properties-common
```

```bash
curl -fsSL https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
```

```bash
sudo add-apt-repository "deb https://download.sublimetext.com/ apt/stable/"
```

```bash
sudo apt install sublime-text
```

## VS code

```bash
sudo snap install --classic code
```

## Postman

```bash
sudo snap install postman
```

## Docker


The download instructions can be taken from the [official docker website](https://docs.docker.com/engine/install/ubuntu/)


## Spotify

```bash
snap install spotify
```

## Sticky Notes

```bash
sudo add-apt-repository ppa:umang/indicator-stickynotes
sudo apt-get update
sudo apt-get install indicator-stickynotes
```

## Blender

```bash
sudo snap install blender --classic
```

## GIMP

```bash
sudo apt install gimp
```

## Kazam : Screen recorder

```bash
sudo apt install kazam
```



## Htop

```bash
sudo snap install htop
```

## Virtual Box

```bash
sudo apt-get update
```

```bash
sudo apt-get install virtualbox
```

```bash
sudo apt-get install virtualbox—ext–pack
```

## Kali Virtualbox

Head over to the following link

```
https://www.kali.org/get-kali/#kali-virtual-machines
```

and download the `.ova` file. Once the download is complete then open it with `Virtialbox`. Start the machine and login using `kali` and `kali` respectively as username and password.


## How to Install Metasploitable in VirtualBox

Head over to the following link

```
https://securingninja.com/how-to-install-metasploitable-in-virtualbox/
```


## Wireshark

```bash
sudo apt update
sudo apt install wireshark
```

## Burpsuite

[Reference](https://delhitrainingcourses.com/blog/install-burp-suite-on-linux-ubuntu/)

Head over to [Burpsuite Releases](https://portswigger.net/burp/releases) and download the `.sh` file for installer.

Then run the installer by

```bash
sh <installer-name>.sh
```

## Binwalk

[Reference](https://blog.eldernode.com/install-binwalk-on-ubuntu-20-04/)

```bash
wget https://github.com/ReFirmLabs/binwalk/archive/master.zip
```

```bash
unzip master.zip
```

```bash
sudo apt update
```

```bash
sudo apt install binwalk
```


## Steghide

```bash
sudo apt update
sudo apt install steghide
```

## Stegsnow

```bash
sudo apt update
sudo apt install stegsnow
```

## Exiftool

```bash
sudo apt install exiftool
```

## Audacity

```bash
sudo apt update
sudo apt install audacity
```

## Sonic Visualizer

```bash
sudo apt update
sudo apt install sonic-visualiser
```

## Nessus

## ISO Files
