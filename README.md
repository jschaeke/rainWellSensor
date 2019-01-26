# Rain well tank sensor MQTT
This project is a simple sketch reading 2 sensors and publishing it to an MQTT topic:
- DHT humidity and temperature sensor
- JSN-SR04T ultrasonic distance sensors

# Hardware
I used a wemos D1 and put the hardware (sensors and voltage converter) inside an electrical box to which I applied silicone to waterproof. The humidity/temperature sensor remains in the box as I noticed the readings halted as the inside of the box got filled up with moist. This way I can detect water leakage inside the box and prevent future failure. Too much moist has also been the reason my initial attempts with an HC-SR04 (outside the box) failed as the sensors got clogged up with water. Currently I am using an JSN-SR04T sensor that I fitted in a drilled hole at the bottom of the box and has been proven to be stable. The whole electrical box hangs on top of my rain well tank and is powered by a 220V powerline that gets activated each time for a couple of seconds when we demand rain water (e.g. flushing toilet or washing machine).

# Software
The readings are sent to an MQTT server. Im my case it's feeding a NodeRed dashboard, that I use to control my domotics, and a InfluxDB/Grafana setup for record keeping.

![boxInside](https://i.ibb.co/YZ8cq1W/IMG-20190126-193104.jpg)
![sensor](https://i.ibb.co/jMdgYTL/IMG-20190125-WA0008.jpg)
![box](https://i.ibb.co/dJQ8yrK/IMG-20180911-191650.jpg)
