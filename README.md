# A Node-RED project that integrates MQTT with e-mail

Simple flow that:
  * Connects to MQTT broker and subscribes to a topic (I've used Mosquitto)
  * Transform incoming message to JSON 
  * Creates new e-mail message (JS function)
  * Sends an e-mail to configured address

The idea is that this sample integration projects sends notification to mobile phone via SMS forwarding by e-mail provider. 
