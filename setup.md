# Setup a new machine

## Download ubuntu server iso and write to usb

## Boot from usb and install

```shell
ip link
sudo ip link set xxx up
sudo dhclient xxx
sudo apt install i3
sudo apt install xinit
startx
```

## Install Chrome

```shell
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
sudo apt -f install
```

## Install Docker

```shell
sudo apt-get update
```

```shell
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
sudo apt-get update
sudo apt-get install docker-ce
```