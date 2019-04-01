# Rain well tank sensor MQTT
This project is a simple sketch reading 2 sensors and publishing it to an MQTT topic:
- DHT humidity and temperature sensor
- JSN-SR04T ultrasonic distance sensors

# Why
To have an idea how much is in the tank and helps to identify a dirty filter when no or little additional water is measured after rain.

# Hardware
I used a wemos D1 pro and placed the hardware (sensors and voltage converter) inside an electrical box to which I applied silicone to waterproof it. The Wemos D1 pro has an external wifi connector that I use for an external wifi antenna mounted on top op the box.  The humidity/temperature sensor remains inside the box as I noticed the readings halted as the box got filled up with moist causing electrical failure. This way I can detect water leakage inside the box and hopefully prevent future failure. Too much moist has also been the reason my initial attempts with an HC-SR04 (that was put outside the box) failed as the sensors got clogged up with water. Currently I am using an JSN-SR04T sensor that I fitted in a drilled hole at the bottom of the box (see pictures) and this has been proven to be stable. The whole electrical box hangs on top of my rain well tank and is powered by a 220V powerline that gets activated each time for a couple of seconds when we demand rain water (e.g. flushing toilet or washing machine).

# Software
The readings are sent to an MQTT server. Im my case it's feeding a NodeRed dashboard, that I use to control my domotics, and an InfluxDB/Grafana setup for record keeping.

![boxInside](https://i.ibb.co/YZ8cq1W/IMG-20190126-193104.jpg)
![sensor](https://i.ibb.co/jMdgYTL/IMG-20190125-WA0008.jpg)
![box](https://i.ibb.co/dJQ8yrK/IMG-20180911-191650.jpg)
![NodeRed](https://i.ibb.co/vJNrVqm/Schermafbeelding-2019-04-01-om-21-47-33.png)
