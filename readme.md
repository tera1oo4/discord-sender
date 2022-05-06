##Install PIP
```
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt update
sudo apt install python3-pip nodejs npm
pip install -r requirements.txt
```

[After that you need to install Docker](https://docs.docker.com/engine/install/ubuntu/)

##Install nodejs dependencies
```
npm install
```

##Make image
```
docker build -t dsender .
```

##Run script single
```
HTTPS_PROXY=https_proxy=https://login:password@ip:port docker run \
    --net=host \
    -e DISCORD_TOKEN='discord_token' \
    -e 'DISCORD_CHANNEL_ID'='912053442397212712' \
    -e 'DISCORD_MESSAGE'='Hi' \
    -it dsender
```

##r run script as daemon
```
SNOOZE_TIME=3 npm run start
```
