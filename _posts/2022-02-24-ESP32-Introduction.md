---
layout: post
title: ESP32 Introduction
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

Introduction to ESP32 chips/boards, Arduino IDE/Toolchains, and ESP32 projects.

---
## Introduction to ESP32 SOCs
**[ESP32](https://www.espressif.com/en/products/socs/esp32)**<br>
a dual-core XTensa LX6 MCU, capable of running at 240 MHz with 520 KB of internal SRAM, ntegrated 2.4 GHz, 802.11 b/g/n Wi-Fi and Bluetooth 4.2 (LE) connectivity <br>
**[ESP32-S3](https://www.espressif.com/en/products/socs/esp32-s3)**<br>
a dual-core XTensa LX7 MCU, capable of running at 240 MHz. Apart from its 512 KB of internal SRAM, it also comes with integrated 2.4 GHz, 802.11 b/g/n Wi-Fi and Bluetooth 5 (LE) connectivity that provides long-range support.<br>
**[ESP32-C3](https://www.espressif.com/en/products/socs/esp32-c3)**<br>
a single-core Wi-Fi and Bluetooth 5 (LE) microcontroller SoC, based on the open-source **RISC-V** architecture.<br>

---
### ESP32 Interfaces and Peripherals
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ESP32_interface_peripherals.png?raw=true)

---
## ESP32-WROOM-32
[Insight Into ESP32 Features & Using It With Arduino IDE](https://lastminuteengineers.com/esp32-arduino-ide-tutorial/)<br>

![](https://lastminuteengineers.b-cdn.net/wp-content/uploads/arduino/ESP32-Hardware-Specifications-Reset-Boot-Buttons-LED-Indicators.jpg)

**Features:**<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ESP32_development_board_features.png?raw=true)

---
### NodeMCU-32S pinout
![](https://github.com/rkuo2000/MCU-course/blob/main/images/NodeMCU-32S_pinout.jpg?raw=true)

---
### ESP32-WROOM-32 pinout
![](https://www.mischianti.org/wp-content/uploads/2021/02/ESP32-wroom-32-pinout-mischianti-1024x551.jpg)

---
### ESP32 CAM pinout
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ESP32-CAM_pinout.jpg?raw=true)
**ESP32-CAM upload code**<br>
![](https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/12/ESP32-CAM-FTDI-programmer-5V-supply.png?w=750&quality=100&strip=all&ssl=1)
[ESP-WHO (face detection and recognition)](https://github.com/espressif/esp-who)<br>
[ESP32-CAM video streaming face recognition](https://randomnerdtutorials.com/esp32-cam-video-streaming-face-recognition-arduino-ide/)<br>
[ESP32-CAM video streaming Web server](https://randomnerdtutorials.com/esp32-cam-video-streaming-web-server-camera-home-assistant/)<br>
**Code:** [ESP32-CAM Web server](https://github.com/rkuo2000/arduino/tree/master/examples/ESP32CAM_CamWebServer)<br>

---
## ESP32-WROVER-B
**Features:**
* Microcontroller: 240MHz Tensilica 32-bit Dual-core CPU Xtensa LX6
* 4MB SPI Flash, **8M PSRAM**
* CPU clock frequency is 80~240MHz
* Operating Voltage: 3.0~3.6V
* Wi-Fi: IEEE 802.11 b/g/n (up to 150Mbps)
* Bluetooth 4.2/BLE

![](https://www.espressif.com/sites/default/files/ESP32-WROVER-B.001.jpeg)

---
### [ESP32-lyraT](https://www.espressif.com/en/products/devkits/esp32-lyrat)
[ESP32-LyraT V4.3 Hardware Reference](https://docs.espressif.com/projects/esp-adf/en/latest/design-guide/dev-boards/board-esp32-lyrat-v4.3.html)<br>
![](https://docs.espressif.com/projects/esp-adf/en/latest/_images/esp32-lyrat-v4.3-layout-with-wrover-e-module.jpg)

---
### ESP32-Vaquita-DSPG Development Board
![](https://github.com/espressif/esp-va-sdk/wiki/va_images/esp32_vaquita_dspg_base_board.png)

---
## EPS32 IDE / Toolchains
### ESP32 Arduino IDE
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Arduino_IDE_software.png?raw=true)
1. Download [Arduino IDE](https://www.arduino.cc/en/Main/Software), then Install on PC
2. Run Arduino
3. Files>Preferences>Setting> URLs = *`https://github.com/espressif/arduino-esp32/releases/download/2.0.2/package_esp32_index.json`*
4. Tools>Board>Board Managers>ESP32 Arduino> select `NodeMCU-32S`
5. Tools>Port> select `COM3` or `/dev/ttyUSB0`
6. Tools>Manager Libraries...> search packages to install
7. Sketch>Include Library>Add .ZIP Library...
8. Download [Sample Codes](https://github.com/rkuo2000/arduino) (click `Code`, then select `Download ZIP`)
9. Uncompress arduino-master.zip, store `samples` folder to *~/Documents/Arduino/*
10. File>Examples> select `01.Basics/Blinky` to `Verify`, then `Upload`
11. Press on IO0 (BOOT) button of NodeMCU-32S to upload code
![](https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/08/boot-button-1.jpg?w=750&quality=100&strip=all&ssl=1)

---
### ESP32 Toolchains
**[ESP-IDF](https://github.com/espressif/esp-idf)**<br>
[Standard Setup of Toolchain for Windows](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/windows-setup.html)<br>
1. run [ESP-IDF Installer (556.65MB)](https://dl.espressif.com/dl/esp-idf-tools-setup-2.4.exe)
2. run ESP-IDF Command Prompt / PowerShell
3. run batch
 - `cd C:/Users/USER/Desktop/esp-idf>`
 - `install.bat`
 - `export.bat`
4. run menuconfig 
 - `cd examples/get-started/hello_world`
 - `idf.py set-target ESP32`
 - `idf.py menuconfig`
5. build sample code (hello_world)
 - `cd examples/get-started/hello_world`
 - `idf.py build`
 - `idf.py –p COM3 flash `
 - `idf.py –p COM3 monitor`

**ESP-IDF using Visual Studio Code**<br>
<iframe width="640" height="360" src="https://www.youtube.com/embed/5IuZ-E8Tmhg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
## ESP32 Github
### [ESP-ADF](https://github.com/espressif/esp-adf)
![](https://github.com/espressif/esp-adf/raw/master/docs/_static/adf_block_diagram.png)

### [ESP-VA-SDK](https://github.com/espressif/esp-va-sdk)

### [ESP-SkaiNet](https://github.com/espressif/esp-skainet)
![](https://github.com/espressif/esp-skainet/raw/master/img/skainet_overview2.png)

### [ESP-SR](https://github.com/espressif/esp-sr)

---
## ESP32 Projects
### [160+ ESP32 Projects, Tutorials and Guides with Arduino IDE](https://randomnerdtutorials.com/projects-esp32/)

**[小狐狸事務所 - 兩個ESP32 飛控板專案](http://yhhuang1966.blogspot.com/2020/03/esp32-espcopter32.html)**<br>

**[BLE Haptic Dual Joystick Controller](https://create.arduino.cc/projecthub/chuartdo/ble-haptic-dual-joystick-controller-31c2c2)**<br>
<table>
<tr>
<td><img src="https://hackster.imgix.net/uploads/attachments/279661/20170319_173513_KUg6E20Z0b.jpg?auto=compress%2Cformat&w=680&h=510&fit=max"></td>
<td><img src="https://hackster.imgix.net/uploads/attachments/278570/gameproject_s3jiixhwzj_lOA6fZMR5d.JPG?auto=compress%2Cformat&w=680&h=510&fit=max"></td>
</tr>
</table>

**[ESP32-BLE-Gamepad](https://github.com/lemmingDev/ESP32-BLE-Gamepad)**<br>
Sample Code: [ESP32_Gamepad_Test](https://github.com/rkuo2000/arduino/tree/master/examples/ESP32_Gamepad_Test)<br>
Android App: [GamePad Tester Lite](https://play.google.com/store/apps/details?id=gamepadtesterlite.saturday.chimera.com.gamepadtesterlite&hl=en)<br>
![](https://play-lh.googleusercontent.com/4xSp1PlSlrTbVfakY41fdMVM7P8eGG13om4ZPO57FpIrDKLUK0wLKoXukBdNJNCotKU=w240-h480-rw)

<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*

