---
layout: post
title: M2M Protocols
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

M2M Protocols include CoAP, MQTT, AMQP, DDS, and LwM2M.

---
## Future of IoT Technology
[Future of IoT Technology: 8 Trends for Businesses to Watch in 2022](https://www.iotforall.com/future-of-iot-technology-8-trends-for-businesses-to-watch-in-2022)
### AIoT - Artificial Intelligence & IoT Technology
<iframe width="677" height="381" src="https://www.youtube.com/embed/UY6xbrcViVw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### IoT Connectivity — 5G, WiFi 6, LPWAN, and Satellites
* 5G: Advanced Mobile Networks
4G LTE is limited by bandwidth. 5G networks however are much faster and can support data processing needed for IoT networks much more efficiently. 
* WiFi 6
The faster that a network of devices can communicate, the more reliable that the system will be.
* LPWAN
Low-power wide-area network connectivity is an emerging technology that is effective for connecting devices with low-bandwidth usage with low bit rates over larger areas.
* Satellite
satellite-powered IoT devices enable humanitarian staff to report emergency incidents to immediately request assistance

### Edge-Computing - Low Latency & Security
Not only can edge computing reduce latency of IoT technology, but it also has potential to increase the security of data processing

### Wearable IoT Technology
* The Future of IOT Smartwatches and Wristbands
wearable IoT technology has immense potential to aid in medical roles due to its ability to keep track of patient vitals.
* AR & VR
Being provided with sensor data and real-time network information on a head mounted display can be very helpful for professionals

### Smart Homes
The rise of Google Assistant, Amazon Echo, Apple’s Siri and other digital assistants have transformed the smart home industry.
Smart home IoT networks are now expanding their ability to automate tasks like lighting, temperature control, and security. These can be configured manually by consumers, or they can be tuned automatically using AI algorithms that review sensor and usage data. 

### Smart Cities
* Smart Streetlights
* Self-driving Shuttles
* IoT Smart Parking
<iframe width="677" height="381" src="https://www.youtube.com/embed/-9s9QkpRzWs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
## M2M Communcation Protocols
![](https://en.idate.org/content/uploads/2017/09/Key_iot_tech.png)

[4 Major IoT Protocols — MQTT, CoAP, AMQP, DDS](https://medium.com/@rinu.gour123/4-major-iot-protocols-mqtt-coap-amqp-dds-46016897c3e9)
![](https://miro.medium.com/max/1400/0*aSC2xYnQyhY-nCgk.jpg)

---
### [CoAP - RFC 7252 The Constrained Application Protocol](https://datatracker.ietf.org/doc/html/rfc7252)<br>
![](https://miro.medium.com/max/1400/0*WOpzdMBn-8DovEHy.jpg)
<br>

---
### [MQTT - The Standard for IoT Messaging](https://mqtt.org/mqtt-specification/)<br>
![](https://miro.medium.com/max/1400/1*7MwXy5N4rx4mAxZ2KZrwJQ.png)
[MQTT vs CoAP, the battle to become the best IoT protocol](https://www.pickdata.net/news/mqtt-vs-coap-best-iot-protocol)<br>
MQTT is preferred over CoAP for mission-critical communications because it can enforce quality of service and ensure message delivery. 
![](https://marvel-b1-cdn.bc0a.com/f00000000017219/documents.trendmicro.com/images/TEx/articles/MQTT-fig-1.jpg)

---
### [AMQP - Advanced Message Queuing Protocol (ISO/IEC 19464:2014)](https://www.amqp.org/)<br>
![](https://miro.medium.com/max/1400/0*7FD4MN_UEJT2tiWn.jpg)

---
### [DDS - Data Distribution Service](https://www.dds-foundation.org/omg-dds-standard/)<br>
![](https://miro.medium.com/max/1400/0*dY0FJCwTzf1LH8Tq.jpg)
![](https://www.dds-foundation.org/wp-content/uploads/2015/07/FIgure-3-a.jpg)
Ref. [What is DDS?](https://www.dds-foundation.org/what-is-dds-3/)

---
### LwM2M (LightWeight Machine-to-Machine protocol)
[LwM2M specification](https://technical.openmobilealliance.org/index.html)<br>
[Overview of LwM2M](https://docs.devicewise.com/Content/GettingStarted/Overview-of-LWM2M.htm)
![](https://docs.devicewise.com/Content/Resources/Images/26804851_462x371.png)
[LwM2M v1.11 slides](https://www.openmobilealliance.org/release/LightweightM2M/Lightweight_Machine_to_Machine-v1_1-OMASpecworks.pdf)<br>
**LwM2M Protocol stack**<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/LwM2M_Protocol_stack.png?raw=true)
![](https://www.yottau.com.tw/download/fc4adac6a5f9f66ca6f357f06e5b591c.png)

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

