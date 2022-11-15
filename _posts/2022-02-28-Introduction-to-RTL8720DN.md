---
layout: post
title:  Introduction to RTL8720DN
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

Introduction to Realtek RTL8720DN.

---
## Introduction to Realtek MCUs

* **RTL8720DN**<br>
Realtek RTL8720DN is a Wi-Fi and Bluetooth IC that supports 2.4GHz and 5GHz dual bands for Wi-Fi communication, and Bluetooth Low Energy (BLE) 5.0. <br>
**BW16 TypeC board**<br>
![](https://www.amebaiot.com/wp-content/uploads/2022/07/bw16_typec/P02.png)

---
### [RTL8720DN typeC](https://www.amebaiot.com/en/amebad-bw16-typec-arduino-getting-started/)
**BW16-TypeC Pinmap**<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/RTL8720DN_BW16_typeC_pin_diagram.png?raw=true)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/RTL8720DN_pin_table.png?raw=true)

---
### setup Arduino IDE
* `Preferences` -> Additional Boards Manager URLs :<br>
  `https://github.com/ambiot/ambd_arduino/raw/master/Arduino_package/package_realtek.com_amebad_index.json`<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ArduinoIDE_Preferences_URLs_RTL8720DN.png?raw=true)

* select `Tools` -> `Board` -> `Boards Manager...`
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ArduinoIDE_Tools_Board_BoardsManager.png?raw=true)

* search Realtek Ambeba boards, then click `Install`
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ArduinoIDE_Board_BoardsManager_install_Realtek_Ambeba_boards.png?raw=true)

* select `(BW16)RTL8720DN`<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ArduinoIDE_Tools_Board_select_RTL8720DN.png?raw=true)

* check Board's name & Port name: `/dev/ttyUSB0`<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/ArduinoIDE_Board_RTL8720DN_ttyUSB0.png?raw=true)

* set UART baud rate to 115200
Tools>Serial Monitor> set baud to 115200

* Ubuntu: chmod /dev/ttyUSB0 available to all users<br>
  `sudo chmod 777 /dev/ttyUSB0`<br>

* first-time using the board
  - Select `Tools` -> `Erase Flash` -> `Enable` to erase flash once<br>
  - Select `Tools` -> `Erase Flash` -> `Disable` for the rest flashing<br>
  - Select `Tools` -> `Auto Upload Mode` -> `Disable`<br>
<br>
* error: Enter Uart Download Mode
![](https://github.com/rkuo2000/MCU-course/blob/main/images/RTL8720DN_error_Enter_Uart_Download_Mode.png?raw=true)
  1. press & hold Burn, then press RST
  2. release RST, then release Burn
  3. upload again
  
<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*

