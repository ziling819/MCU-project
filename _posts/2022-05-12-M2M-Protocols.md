---
layout: post
title: M2M Protocols
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

M2M Protocols include CoAP, MQTT, AMQP, DDS, and LwM2M.

---
## M2M Communcation Protocols
[4 Major IoT Protocols — MQTT, CoAP, AMQP, DDS](https://medium.com/@rinu.gour123/4-major-iot-protocols-mqtt-coap-amqp-dds-46016897c3e9)
![](https://miro.medium.com/max/1400/0*aSC2xYnQyhY-nCgk.jpg)

### [CoAP - RFC 7252 The Constrained Application Protocol](https://datatracker.ietf.org/doc/html/rfc7252)<br>
![](https://miro.medium.com/max/1400/0*WOpzdMBn-8DovEHy.jpg)
<br>

### [MQTT - The Standard for IoT Messaging](https://mqtt.org/mqtt-specification/)<br>
![](https://miro.medium.com/max/1400/1*7MwXy5N4rx4mAxZ2KZrwJQ.png)
[MQTT vs CoAP, the battle to become the best IoT protocol](https://www.pickdata.net/news/mqtt-vs-coap-best-iot-protocol)<br>
MQTT is preferred over CoAP for mission-critical communications because it can enforce quality of service and ensure message delivery. 
![](https://marvel-b1-cdn.bc0a.com/f00000000017219/documents.trendmicro.com/images/TEx/articles/MQTT-fig-1.jpg)


### [AMQP - Advanced Message Queuing Protocol (ISO/IEC 19464:2014)](https://www.amqp.org/)<br>
![](https://miro.medium.com/max/1400/0*7FD4MN_UEJT2tiWn.jpg)

### [DDS - Data Distribution Service](https://www.dds-foundation.org/omg-dds-standard/)<br>
![](https://miro.medium.com/max/1400/0*dY0FJCwTzf1LH8Tq.jpg)
![](https://www.dds-foundation.org/wp-content/uploads/2015/07/FIgure-3-a.jpg)
Ref. [What is DDS?](https://www.dds-foundation.org/what-is-dds-3/)

---
### [Salesforce IoT – Internet of Things Clouds](https://data-flair.training/blogs/salesforce-iot/)

--- 
### NodeMCU-32S pinout
![](https://github.com/rkuo2000/MCU-course/blob/main/images/NodeMCU-32S_pinout.jpg?raw=true)

---
## CoAP example
### Arduino Library: CoAP simple library
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Arduino_Library_CoAP_simple_library.png?raw=true)

### [Homework]: ESP32_CoAP_server.ino
Examples>CoAP simple library>esp32
* code modifications
  - modify LEDpin to 2
  - modify SSID & Passwd
  - add to print out LEDSTATE in callback
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Examples_CoAP_simple_library_esp32.png?raw=true)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Examples_CoAP_simple_library_esp32_monitor.png?raw=true)
* Ubuntu install **libcoap**<br>
`sudo apt install libcoap2-bin`<br>
* [libcoap coap-client](https://libcoap.net/doc/reference/4.2.1/man_coap-client.html)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Examples_Ubuntu_libcoap_coap-client.png?raw=true)

### Sketch: [ESP32_Coap_client.ino](https://github.com/rkuo2000/arduino/blob/master/examples/ESP32/ESP32_CoAP_client/ESP32_CoAP_client.ino)<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Sketch_ESP32_CoAP_client.png?raw=true)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Sketch_ESP32_CoAP_client_monitor.png?raw=true)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Sketch_ESP32_CoAP_server_monitor.png?raw=true)

---
## MQTT example
### Arduino Library: Adafruit MQTT Library
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Arduino_Library_MQTT.png?raw=true)

### Examples>ArduinoMqttClient>WiFiSimpleReceive
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Sketch_ESP32_MQTT_mosquitto_Receiver.png?raw=true)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Sketch_ESP32_MQTT_mosquitto_Receiver_monitor.png?raw=true)

### Examples>ArduinoMqttClient>WiFiSimpleSender
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Sketch_ESP32_MQTT_mosquitto_Sender.png?raw=true)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Sketch_ESP32_MQTT_mosquitto_Sender_monitor.png?raw=true)

### [Homework]: ESP32_MQTT_mosquitto_Receiver & Sender
* work with another classmate
* one running ESP32_MQTT_mosquitto_Reciever.ino, the other running ESP32_MQTT_mosquitto_Sender.ino

---
### Examples>Adafruit MQTT Library>adafruitio_secure_esp32
* Modify Modify WLAN_SSID & WLAN_PASS
* Sign-In https://io.adafruit.com/ to get KEY
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Examples_Adafruit_MQTT_Library_adafruitio_secure_esp32.png?raw=true)
* Run adafruitio_secure_esp32.ino on ESP32
* Open browser at io.adafruit.com/yourname/feeds/test
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Examples_Adafruit_MQTT_Library_adafruitio_secure_esp32_dashboard.png?raw=true)

### [Homework]: ESP32 with HTU21D/DHT11 update humidity & temperature to io.adafruit.com/yourname

<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*

