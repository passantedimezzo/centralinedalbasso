# #centralinedalbasso
Per costruirsi una centralina servono su per giu una 30ina di euro
i pezzi da ordinare online sono questi ...
tutto opensource ... e dal basso
... ci va un mesetto per fare arrivare i pezzi,
va poi montata seguendo le istruzioni,
piazzata sul balcone, terrazzo o finestra, a tiro di wifi 
e attaccata alla corrente.
Consuma meno di 1 watt, quindi il costo della corrente dovrebbe essere all'incirca di un paio di euro all'anno.

- twitter: https://twitter.com/passantedimezzo
- #centralinedalbasso: https://twitter.com/hashtag/centralinedalbasso
- le mappe: http://bologna.maps.luftdaten.info/

![Centraline dal Basso](https://github.com/passantedimezzo/centralinedalbasso/blob/master/C83zbN_WAAAclAG.jpg)

 
## Le istruzioni per il montaggio le trovi qui 
  https://twitter.com/passantedimezzo/status/850919842333036544
  
#### update: sono disponibili i firmware in italiano e inglese
  - firmware italiano: https://www.madavi.de/sensor/update/data/latest_it.bin
  - firmware inglese: https://www.madavi.de/sensor/update/data/latest_en.bin
  
 
## Lista della spesa per centralina pm10 pm2.5
 
### Questi sono i 4 pezzi che servono, da ordinare online
 
1) #### sensore pm10-pm2.5  (21.80$)
   https://it.aliexpress.com/item/nova-PM-sensor-SDS011-High-precision-laser-pm2-5-air-quality-detection-sensor-module-Super-dust/32617788139.html
 
2) #### processore ch340 NodeMcu v3  (2.95$)
   https://it.aliexpress.com/item/New-Wireless-module-CH340-NodeMcu-V3-Lua-WIFI-Internet-of-Things-development-board-based-ESP8266/32549862093.html
 
3) #### cavetti (0.60$)
   https://it.aliexpress.com/item/40pcs-lot-10cm-2-54mm-1pin-Female-to-Female-jumper-wire-Dupont-cable/32378478740.html
 
4) #### sensore temperatura/umidita' DHT22 (2.32$)
   https://it.aliexpress.com/item/1pcs-DHT22-digital-temperature-and-humidity-sensor-Temperature-and-humidity-module-AM2302-replace-SHT11-SHT15-Free/1059369726.html


## Schema elettrico nodemcu v3 sds011
![Schema elettrico nodemcu v3 sds011](https://github.com/passantedimezzo/centralinedalbasso/blob/master/nodemcu-v3-schaltplan-sds011.jpg)

### Collegamenti SDS011
```
SDS011 Pin 1 -> Pin D1 / GPIO5
SDS011 Pin 2 -> Pin D2 / GPIO4
SDS011 Pin 3 -> GND
SDS011 Pin 4 -> unused
SDS011 Pin 5 -> VU (NodeMCU v3) / VIN (NodeMCU v1,v2)
SDS011 Pin 6 -> unused
SDS011 Pin 7 -> unused
```

### Collegamenti DHT22
```
DHT22 Pin 1 -> Pin 3V3 (3.3V)
DHT22 Pin 2 -> Pin D7 (GPIO13)
DHT22 Pin 3 -> unused
DHT22 Pin 4 -> Pin GND
```

### Collegamenti BME280
```
BME280 Vcc => 3V3
BME280 Gnd => GND
BME280 SDA => D3
BME280 SCL => D4
```
