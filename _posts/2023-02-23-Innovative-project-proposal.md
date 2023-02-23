---
layout: post
title: Innovative Project Proposal
author: [Wu Zi-Ling]
category: [Lecture]
tags: [jekyll, ai]
---

This homework is to propose an innovative project and describe the key features, list all Design Considerations and the required technologies, then draw the System Block Diagram.

---
## Homework Report Format
**Contents:**<br>
* **應用與功能說明**
  - Specify the future home application, and Describe the key features
  - Describe the key features which may be applied to the home space (kitchen, living room, play room, study room, bed room)
* **設計考量與所需相關技術**
  - List all design considerations and the required technologies
* **系統方塊圖**
  - Draw a System Block Diagram

---
## 家用料理機器人

### 應用功能說明
1. 操作廚具：咖啡機＋果汁機＋烤麵包機＋微波爐+烤箱+氣炸鍋
2. 存取冰箱：辨識食物, 存放食材，或取出食材, 送至廚具

### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:垂直升降式手臂 or 懸吊式手臂
2. 移動方式:兩輪 or 滑軌懸吊
3. 供電方式:鋰電池
4. 聯網方式:WiFi或BT to 手機

**所需相關技術：**
1. 滑軌式機器手臂 ＆ 軟式夾具
2. 食物辨識分類：Jetson-Nano + IMX219
3. 電子鼻：氣味感測與辨識 MQ2

### 系統方塊圖
![](https://github.com/ziling819/MCU-project/blob/main/images/ESP32_RoboCar.jpg?raw=true)
### 參考 
<iframe width="1239" height="697" src="https://www.youtube.com/embed/bdKcid21p6I" title="我獲得了一台「神級機器人」？！從破爛機器人到最強機器人的成長過程！【Roblox 機械方塊】" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
---


<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


