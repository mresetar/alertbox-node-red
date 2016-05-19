# A Node-RED project that integrates MQTT with e-mail

Simple flow that:
  * Connects to MQTT broker and subscribes to a topic (I've used Mosquitto)
  * Transform incoming message to JSON 
  * Creates new e-mail message (JS function)
  * Sends an e-mail to configured address

The idea is that this sample integration projects sends notification to mobile phone via SMS forwarding by e-mail provider. 

## To run this project via Docker container

First pull down node-red container and then run it. 

```bash
docker pull cpswan/node-red

# This is already done if you've cloned this repo
curl -k https://raw.githubusercontent.com/node-red/node-red/master/settings.js -o settings.js

# In next command as a volume I've used location of git project location locally. 
docker run --name=nodered -d -v /c/Users/miroslavresetar/git/alertbox-node-red:/root/.node-red -p 1881:1880 cpswan/node-red
```

If you're using VM for container go to Node-RED flow by going to URL:

[http://192.168.99.100:1881](http://192.168.99.100:1881)
