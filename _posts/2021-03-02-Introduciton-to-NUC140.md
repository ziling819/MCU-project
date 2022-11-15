---
layout: post
title: Introduction to NUC140
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

Introduction to NUC140 and its Learning Board.

---
## NUC140 Key Features
### Core
* Cortex™-M0 processor
* Max frequency of 72 MHz
* Operating voltage: 2.5V to 5.5V
* Temperature range: - 40 ℃ ~ 105 ℃

### Memory
* 128 KB of flash memory
* 16 KB of SRAM  
* 4 KB of Data Flash
* ISP ( In-System Programming )
* ICP ( In-Circuit Programming )
* IAP ( In-Application Programming )

### ADC
* Up to 8 channels
* 12-bit resolution
* Up to 800 kSPS
* A/D conversion started by PWM
* ± 1 ℃ accurate Temperature sensor

### PWM
* Up to eight-channel PWM or three complementary paired PWM outputs
* Period/duty trigger ADC function

### Connectivity
* Up to one SPI s ( up to 36 MHz )
* Up to two I²C s ( up to 400 kHz )
* Up to six UART s ( up to 1 Mbps )
* Up to three  ISO-7816-3
* Up to two  Bosch CAN 2.0A/B
* USB 2.0 full speed
* 16/8 bits EBI interface

### Clock Control
* 4 to 24 MHz external crystal oscillator
* 22.1184 MHz internal RC oscillator ( ± 1 % accuracy at 25 ℃ , 5V )

**Datasheet:** [NUC140VE3CN](https://www.nuvoton.com/export/resource-files/DA00-NUC140ENF1.pdf)
 	
--- 
## NUC140 Learning Board
![](https://direct.nuvoton.com/img/cms/NL-NUC140V.jpg)

### Trouble Shooting
* *PC USB port supply maximum current of 500mA*
* *When shorted circuits or over-drive current from external electronic circuits or peripheral modules, PC may cut off the power of the USB port --> Just reboot the PC !*
* *NUC140 chip is very hot when the learning board is running, the board may be damaged due to pin mis-connected to high voltage (>5V) --> Replace the learning board !!!*
* *LCD has no display when it is cracked or damaged --> Replace the LCD !!!*
* *LCD has no display when its soft cable on the back of the board was unplugged and did not reconnect properly --> User need to reconnect the LCD soft cable to the interface socket tightly*

---


<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


