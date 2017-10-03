# FindMyArduino
FindMyArduino example inspired by Apple's Find My iPhone, locate your Arduino by using GPS. The best way to find back your Arduino if it walks away or gets stolen.

### Introduction
During our minor Smart Industry we have to build something for the Smart Room. This something is based on the Arduino knock off ESP32, which is a nice IoT hardware platform compatible with the Arduino IDE.

![fma_ui](https://cldup.com/dTxpPi9lDf.thumb.png)

### Features
- **Realtime** location using Google Maps
- Remembers last known location
- Shows last update date
- Shows Arduino connection status
- Comes with a simple API

### Hardware
The hardware is based on the ESP32 and a GY-GPS6MV2 GPS module. These components are Arduino compatible.

![fma_hardware](https://cldup.com/dTxpPi9lDf.thumb.png)

![fma_circuit](https://cldup.com/dTxpPi9lDf.thumb.png)

![fma_esp32](https://cldup.com/dTxpPi9lDf.thumb.png)

![fma_gps](https://cldup.com/dTxpPi9lDf.thumb.png)

### Software
The software is based on the DemoProgram by Franz. If you don't have access to this code I refer you to the following links:

[http://arduinostuff.blogspot.nl/2014/05/neo6mv2-gps-module-with-arduino-uno-how.html](http://arduinostuff.blogspot.nl/2014/05/neo6mv2-gps-module-with-arduino-uno-how.html)
[http://www.ayomaonline.com/iot/gy-gps6mv2-neo6mv2-neo-6m-gps-module-with-arduino-usb-ttl/](http://www.ayomaonline.com/iot/gy-gps6mv2-neo6mv2-neo-6m-gps-module-with-arduino-usb-ttl/)
[https://github.com/mikalhart/TinyGPS](https://github.com/mikalhart/TinyGPS)

This project is build using PHP and Javascript. Powered by the Google Maps API.

### Interoperability
One of the assignments is to make your project interact with other projects. In this case FindMyArduino is just a sensor, it can't do anything else than pulsing GPS coordinates. This project includes a very simple API to get the current coordinates. Other students and their project are able to use this information in their systems.

The API can be accessed using two methods: RAW and JSON. The URL is currently accessible without authentication:
http://www.yoururl.com/gps.php?api=json
```
["5.94978","51.98896",1506511059]
```
http://www.yoururl.com/gps.php?api=raw
```
51.98896-5.94978
```

It will return the latest lattitude, longtitude and timestamp.