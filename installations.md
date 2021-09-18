# My installations for a new OS

## Pre-requisites

```bash
sudo snap install curl
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
