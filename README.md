# node-red-contrib-mqttenv

This is a fork of the original [node-red](https://github.com/node-red/node-red) [mqtt node](https://github.com/node-red/node-red/tree/master/nodes/core/io) with the added feature that the broker address can resolve environment variables. This allows for semi dynamic changeing of brokers without changing the actual flow that is loaded by node-red.

Credits to artcom for his [node-red-contrib-mqtt-env](https://github.com/artcom/node-red-contrib-mqtt-env) node that is built on the same idea. A new node was created because this inital node by artcom dosen't seem to be under development as it is built on the old mqtt node that now is deprecated. Also a difference between artcoms node and this one is that this node can resolve several env variables and will concatinate it into the broker url.

## Install
Run the following command in your node-red directory.
```
npm install node-red-contrib-mqttenv
```

## Usage
Before running node-red make sure that you have an environment variable set. eg `export FOO=abc`.

Add a mqttenv node to your flow. Configure a mqtt broker as per usual. Then in the Server field where you would enter the url you can add your environment varibles eg.`%FOO%.server.com` which once the node is running will be resolved to `abc.server.com`
