# ZKVerifyValidator
How to setup ZKVerfiy Validator node to send zk proofs

zkVerify is a high-performant, public, and decentralized blockchain dedicated to zero-knowledge proof verification. It provides a modular and composable approach for ZK apps to verify proofs.

Docs : https://docs.zkverify.io/

# Join Crypto Console Community

Join TG : [Crypto Console Telegram](https://t.me/cryptoconsol) 

Follow X : [Crypto Console Twitter](https://www.x.com/cryptoconsol) 

Subscribe : [Crypto Console Youtube](https://www.youtube.com/@cryptoconsole)

---

## Hardware requirements:

| **Hardware** | **Minimum Requirement** |
|--------------|-------------------------|
| **CPU**      | 2 Cores                 |
| **RAM**      | 2 GB                    |
| **Disk**     | 150  GB  SSD            |

---

# VPS Options

💻 Contabo VPS Deals 🚀 Buy with Credit Card/Paypal/Crypto Credit card : 

Get powerful VPS solutions with these direct links:  


| **VPS** | **Direct Link**                      | **Specs**                                                                                              |
|---------|--------------------------------------|--------------------------------------------------------------------------------------------------------|
| VPS 1   | [Contabo VPS 1](https://www.jdoqocy.com/click-101278318-15692486) | 4 vCPU Cores, 4 GB RAM, 100 GB NVMe or 400 GB SSD     |
| VPS 2   | [Contabo VPS 2](https://www.anrdoezrs.net/click-101278318-13796472) | 6 vCPU Cores, 16 GB RAM, 200 GB NVMe or 400 GB SSD  |
| VPS 3   | [Contabo VPS 3](https://www.dpbolvw.net/click-101278318-13796474) | 8 vCPU Cores, 24 GB RAM, 300 GB NVMe or 1.2 TB SSD    |
| VPS 4   | [Contabo VPS 4](https://www.anrdoezrs.net/click-101278318-13796476) | 12 vCPU Cores, 48 GB RAM, 400 GB NVMe or 1.6 TB SSD |


💡 **Get started with the perfect VPS for your needs!** 🚀

---


### Update and Upgrade VPS

```
sudo apt update && sudo apt upgrade
sudo apt-get install ca-certificates curl
```

### Install Docker:

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg  
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null  
sudo apt-get update  
sudo apt-get install -y docker-ce docker-ce-cli containerd.io  
docker --version  
```
### Install Docker-Compose:

```
VER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep tag_name | cut -d '"' -f 4)  
sudo curl -L "https://github.com/docker/compose/releases/download/$VER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose  
sudo chmod +x /usr/local/bin/docker-compose  
docker-compose --version  
```

### Docker Permission to User

```
sudo groupadd docker  
sudo usermod -aG docker $USER  
newgrp docker
```

### Add user

**Change the console to your desired name**

```
sudo useradd -m -s /bin/bash console
sudo usermod -aG docker console
```

### Set user password for security

```
sudo passwd console
```

### Change user

Change console to your username

```
su - console
```

### Clone Repo

```
git clone https://github.com/zkVerify/compose-zkverify-simplified.git
cd compose-zkverify-simplified
```

### Initailize Node

```
./scripts/init.sh
```

### Start Node

```
./scripts/start.sh
```

### Docker compose

**Change console to your username**
 
```
docker compose -f /home/console/compose-zkverify-simplified/deployments/validator-node/testnet/docker-compose.yml up -d
```

### Update node

```
cd ~/compose-zkverify-simplified
git pull
./scripts/update.sh
```

### Check logs 

```
docker logs -f validator-node
```

---

Watch the video to setup 
 

Node dashboard : https://testnet-telemetry.zkverify.io/#/

Download Wallet : https://www.subwallet.app/download.html?lang=1

Faucet : https://zkverify-faucet.zkverify.io/

RPC : https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Ftestnet-rpc.zkverify.io#/staking

---

Follow : https://x.com/cryptoconsol

Join : https://t.me/cryptoconsol
