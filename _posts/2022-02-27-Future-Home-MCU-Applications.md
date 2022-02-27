---
layout: post
title: Future Home MCU Applications (Homework)
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

This homework is to specify a Future Home application and describe the key features, list all Design Considerations and the required technologies, then draw a System Block Diagram.

---
## Futre Home MCU Applications
**Service Robots:**<br>

![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_robots.png?raw=true)

---
**Home Spaces:**<br>

![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_spaces.png?raw=true)

---
### Homework Report
**Contents:**<br>
* **應用與功能說明**
  - Specify the future home application, and Describe the key features
  - Describe the key features which may be applied to the home space (kitchen, living room, play room, study room, bed room)
* **設計考量與所需相關技術**
  - List all design considerations and the required technologies
* **系統方塊圖**
  - Draw a System Block Diagram

---
## 家庭巡檢機器人
### 應用功能說明
1. 溫濕度感測 
2. 生活紀錄
3. 遙控家電

### 設計考量與相關技術
**系統設計考量：**<br>
1. 移動方式:共軸雙旋翼
2. 供電方式:電池＋自動充電
3. 聯網方式: WiFi 或 BLE to中控電腦

**所需相關技術：**
1. 飛行姿態偵測與控制: ESP32 + MPU6050 + PID controller
2. 溫濕度感測 & 瓦斯感測: DHT11 + MQ2
3. 紅外線遙控: IR-LED 
4. 影像傳輸: ESP32-CAM module
5. 服務器程式設計: Jetson-Nano (2GB)
  - 影像物件偵測辨識: CSL-YOLO
  - 任務規劃控制: Mission Planner with Floorplan
6. 手機操控程式設計: MIT AppInventor2 

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_flying_robot.png?raw=true)

---
## 組合式食物料理機
### 應用功能說明
1. 組合式機構:冰箱+微波爐+烤箱+氣炸鍋+烤麵包機+果汁機+調酒機
2. 輸入食物：辨識食物, 並分類排序擺放（目標為可冷藏類食物）
3. 液體容器：水，牛奶, 飲料, 調酒
4. 推薦食譜：依車用小型冰箱之內容物, 建議可能之組合餐點
5. 輸送食物：輸送帶傳送食物至果汁機+微波爐+烤箱+氣炸鍋+烤麵包機
6. 湯品飲料：果汁機+調酒機

### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:組合式小家電
2. 供電方式:有線
3. 聯網方式:WiFi或BT to 手機

**所需相關技術：**
1. 組合式機構設計
2. 網頁界面：ESP32 WebServer
3. 食物辨識分類：Jetson-Nano
4. 食物溫度感測：DS18B20
5. 氣味感測：MQ2
6. 小型水泵

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_integrated_food_generator.png?raw=true)

---
## 早晨喚醒系統
### 應用功能說明
1. 照度偵測
2. 藍牙手環監測睡眠品質,並保存睡眠動態紀錄
3. 手勢偵測與遙控
3. 鬧鐘喚醒功能：播放預設音檔.Wav, 或播放網路電台(PAM8403+8ohm speaker)
4. 遙控電動窗簾：紅外線遙控 (IR-LED)
5. 操控燈光：智慧燈泡＋手勢辨識 (TinyML)

### 設計考量與相關技術
**系統設計考量：**<br>
1. 感測方式:照度,手環動態及手勢
2. 供電方式:音箱用有線電源,手環用電池
3. 聯網方式:WiFi或BT to 手機

**所需相關技術：**
1. 照度感測: ADC界面讀取光敏電阻(GL5516)
2. 睡眠品質監測：藍牙穿戴式手環(ESP32+MPU6050), 運用三軸加速器偵測睡眠動態
3. 手勢偵測：MPU6050感測手勢動作之三軸加速器數值, 利用TinyML進行AI手勢辨識
4. 網路電台播放：ESP32 Internet Radio player
5. 智慧燈泡連接：AWS Alexa介接, 或藍牙命令操控燈光

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_wakeup_system.png?raw=true)

---
## 伴學機器人
### 應用功能說明
1. 外語學習
2. 學齡前遊戲互動

### 設計考量與相關技術
**系統設計考量：**<br>
1. 移動方式：球形滾動
2. 供電方式：鋰電池
3. 互動方式：LCD顯示模組 + 語音輸出入 + 肢體動作 + 指頭操作
4. 作業系統：採用Android OS

**所需相關技術：**
1. 影像物件識別： 執行 CSL-YOLO模型進行辨識(Jetson Nano)
2. 語音辨識與輸出： Speech Recognition & Text-To-Speech (AppInventor 2)
3. 外語教學：AI對答
4. 指頭操作：觸控 & 吸盤式電磁頭
5. 互動教具：字卡, 跳棋, ...

### 系統方塊圖
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Future_Home_interactive_companion_robot.png?raw=true)
<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


