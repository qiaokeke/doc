### install the dependencies
```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
### Add The Docker Repository
```
vim /etc/apt/sources.list.d/docker.list
deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt update
```
### Install Docker CE
```
sudo apt install docker-ce
```
