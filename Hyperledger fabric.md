# BLOCKCHAIN
**This is my repository regarding the Blockchain which contain Hyperledger Fabric deploy.**

![IMG_20230705_135651_873](https://github.com/Vedkkp/Blockchain/assets/100022997/7a3689fd-681c-4a74-8b48-d3d13d8aaab0)

# HYPERLEDGER-FABRIC

TO INITIATE THE FIRST HYPERLEDGER FABRIC NETWORK, WE WILL UTILIZE THE FABRIC-SAMPLES REPOSITORY. THIS REPOSITORY CONSISTS OF CLI TOOL BINARIES AND FABRIC DOCKER IMAGES, WHICH ARE ESSENTIAL FOR COMPREHENDING AND UTILIZING THE FUNDAMENTALS OF FABRIC. BEFORE COMMENCING THE PROJECT, IT IS NECESSARY TO INSTALL THE FOLLOWING DEPENDENCIES:

## 1. INSTALL DOCKER

For this Some of the codes from **Shubham Tatvamasi** are used to install the docker.


### Quick Install
```bash
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
```
---

Install packages:
```bash
sudo apt update
sudo apt install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release \
    jq
```

Add Docker’s official GPG key:
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

Setup repository:
```bash
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Install Docker Engine:
```bash
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io
```

Add your user to the docker group:
```bash
sudo usermod -aG docker $USER
```

### Docker Compose

Download the current stable release of Docker Compose:
```bash
COMPOSE_VERSION=$(curl -s "https://api.github.com/repos/docker/compose/tags" | jq -r '.[0].name')
sudo curl -L "https://github.com/docker/compose/releases/download/${COMPOSE_VERSION}/docker-compose-$(uname -s)-$(uname -m)" \
  -o /usr/local/bin/docker-compose
```

Apply executable permissions to the binary:
```bash
sudo chmod +x /usr/local/bin/docker-compose
```


    sudo apt-get -y install docker-compose
    

## 2. INSTALL GOLANG-GO  

```bash
sudo apt install golang-go
```

## 3. INSTALL JQ


```bash
sudo apt install jq
```  

## 4. INSTALL NODE/JAVA  

```bash
sudo apt install npm
npm install node
```  

## 5. INSTALLING FABRIC-SAMPLES REPOSITORY  

```bash
curl -sSLO https://raw.githubusercontent.com/hyperledger/fabric/main/scripts/install-fabric.sh && chmod +x install-fabric.sh
```  

THEN YOU CAN PULL DOCKER CONTAINERS BY RUNNING ONE OF THESE COMMANDS:


```bash
./install-fabric.sh docker samples
./install-fabric.sh d s
```  

TO INSTALL BINARIES FOR FABRIC SAMPLES YOU CAN USE THE COMMAND BELOW:

```bash
./install-fabric.sh binary
```

## BUILDING FIRST NETWORK 

1.NAVIGATE THROUGH THE FABRIC-SAMPLES FOLDER AND THEN THROUGH THE TEST NETWORK FOLDER WHERE YOU CAN FIND SCRIPT FILES USING THESE WE CAN RUN OUR NETWORK.

```bash
cd fabric-samples/test-network
```

2.WE WOULD BE RUNNING ./NETWORK.SH DOWN COMMAND TO REMOVE ANY PREVIOUS NETWORK CONTAINERS OR ARTIFACTS THAT STILL EXIST.

```bash
./network.sh down
```

3.WE CAN BRING UP A NETWORK USING THE FOLLOWING COMMAND. THIS COMMAND CREATES A FABRIC NETWORK THAT CONSISTS OF TWO PEER NODES AND ONE ORDERING NODE.

```bash
 ./network.sh up
 ```

NOW OUR FIRST HYPERLEDGER FABRIC NETWORK IS SUCCESSFULLY RUNNING.










