# MQTT2MongoDB

A simple Python project that listen to one or more MQTT topics and save all the incoming messages on a MongoDB database, as some sort of logger.

## Requirements

- Python 3.x (tested on 3.7)
- Ubuntu (not tested on other OS)
- MQTT broker
- MongoDB server
- Libraries:
    * pymongo
    * paho-mqtt


## Format of a Mongo document

{'_id': ObjectId('5e7fd8aebead35c5562e2d56'),
 'topic': 'test',
 'payload': '{"Temperature":10,"Humidity":50}',
 'qos': 0,
 'timestamp': 1585436846,
 'datetime': '29/03/2020 04:37:26'}


- Getting timestamp of received messages right when they arrive, by systemcall getting datetime and temp and humidty 
