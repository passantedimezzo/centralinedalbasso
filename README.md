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

  http://luftdaten.info/it/traduzione-delle-istruzioni-per-il-montaggio-del-sensore-di-polveri-sottili/ (work in progress)
  e qui
  https://twitter.com/passantedimezzo/status/850919842333036544
  
#### update: sono disponibili i firmware in italiano e inglese
  - firmware italiano: https://www.madavi.de/sensor/update/data/latest_it.bin
  - firmware inglese: https://www.madavi.de/sensor/update/data/latest_en.bin
  
 
## Lista della spesa per centralina pm10 pm2.5
 
### Questi sono i 4 pezzi che servono, da ordinare online
 
1) #### sensore pm10-pm2.5  (21.80$)
   https://it.aliexpress.com/item/nova-PM-sensor-SDS011-High-precision-laser-pm2-5-air-quality-detection-sensor-module-Super-dust/32617788139.html
 
2) #### processore ch340 NodeMcu v3  (2.95$)
   https://it.aliexpress.com/item/32647690484.html
 
3) #### cavetti (0.60$)
   https://it.aliexpress.com/item/40pcs-lot-10cm-2-54mm-1pin-Female-to-Female-jumper-wire-Dupont-cable/32378478740.html
 
4) #### sensore temperatura/umidita' DHT22 (2.32$) (selezionare Type A)
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
BME280 VCC => 3V3
BME280 GND => GND
BME280 SDA => D3 (GPIO0)
BME280 SCL => D4 (GPIO2)
```

### Collegamenti LCD1602
```
LCD1602 VCC => 3V3
LCD1602 GND => GND
LCD1602 SDA => D3 (GPIO0)
LCD1602 SCL => D4 (GPIO2)
```

### Pannello di configurazione
![Pannello di configurazione](https://github.com/passantedimezzo/centralinedalbasso/blob/master/config.jpg)

### 
script python per leggere direttamente i valori dal sensore sds011

https://gist.github.com/netmaniac/a6414149a5a09ba1ebf702ff8d5056c5

es:
```
> sudo python nova_sensor.py
18 Apr 2017 15:29:32.092517: PM 2.5: 9.8 μg/m^3  PM 10: 20.8 μg/m^3
18 Apr 2017 15:29:35.087666: PM 2.5: 9.8 μg/m^3  PM 10: 20.3 μg/m^3
18 Apr 2017 15:29:41.077433: PM 2.5: 9.8 μg/m^3  PM 10: 20.1 μg/m^3
18 Apr 2017 15:29:44.071522: PM 2.5: 9.5 μg/m^3  PM 10: 20.1 μg/m^3
18 Apr 2017 15:29:51.048019: PM 2.5: 9.3 μg/m^3  PM 10: 20.5 μg/m^3
```
### Video presentazione di Jan Lutz (luftdaten.info)
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/hTSu_npeuuo/0.jpg)](https://www.youtube.com/watch?v=hTSu_npeuuo)


### Video montaggio con tecnica belga utilizzando una bottiglia PET
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/fxTSLfomtbU/maxresdefault.jpg)](https://www.youtube.com/watch?v=fxTSLfomtbU)

### Qui tutte le puntate dell'inchiesta sul passante di bologna (le prime 3 per @Internazionale) firmate da WM2 e @vukbuk

1) <a href="https://t.co/HaMI4RUYGy">https://t.co/HaMI4RUYGy</a><br><br>
2) <a href="https://t.co/j3JM932gBt">https://t.co/j3JM932gBt</a><br><br>
3) <a href="https://t.co/nKmKvcYbrm">https://t.co/nKmKvcYbrm</a><br><br>
4) <a href="https://t.co/YN3DXR41de">https://t.co/YN3DXR41de</a><br><br>
5) <a href="https://t.co/SO26PPjIKy">https://t.co/SO26PPjIKy</a><br><br>
6) <a href="https://t.co/rBGSmjyNgL">https://t.co/rBGSmjyNgL</a><br><br>
7) <a href="https://t.co/OVtVXEki9J">https://t.co/OVtVXEki9J</a><br><br>
8) <a href="https://t.co/VD9NSyzbER">https://t.co/VD9NSyzbER</a></p> 

