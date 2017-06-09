# Node-RED Snippets

## Node-RED flow to read Data from sensor #1495

```
[{"id":"4616ba3.20c5f44","type":"debug","z":"b67d3b5e.4982c8","name":"","active":true,"console":"false","complete":"payload","x":793,"y":839,"wires":[]},{"id":"58629b81.4e94b4","type":"inject","z":"b67d3b5e.4982c8","name":"","topic":"","payload":"","payloadType":"date","repeat":"","crontab":"","once":false,"x":151,"y":825,"wires":[["a52e54d3.da8d78"]]},{"id":"a52e54d3.da8d78","type":"http request","z":"b67d3b5e.4982c8","name":"luftsensor #1495","method":"GET","ret":"txt","url":"http://api.luftdaten.info/v1/sensor/1495/","x":337,"y":836,"wires":[["9c9380d2.d1489"]]},{"id":"9c9380d2.d1489","type":"json","z":"b67d3b5e.4982c8","name":"","x":494,"y":855,"wires":[["20427046.fe445","39168d6f.d5f242"]]},{"id":"20427046.fe445","type":"function","z":"b67d3b5e.4982c8","name":"centralinedalbasso","func":"pm10 = msg.payload[0].sensordatavalues[0].value;\npm25 = msg.payload[0].sensordatavalues[1].value;\nmsg.payload = \"Sensor #1495: PM10 \" + pm10 + \"ng/m3 PM2.5 \" + pm25 + \"ng/m3\";\nmsg.payload = '\"' + msg.payload + '\"';\nreturn msg;","outputs":1,"noerr":0,"x":614,"y":951,"wires":[["4616ba3.20c5f44","b5aff926.4a5008"]]},{"id":"39168d6f.d5f242","type":"freeboard","z":"b67d3b5e.4982c8","name":"luftsensor #1495","x":622,"y":1027,"wires":[]}]
```
