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
## 保衛機器人

### 應用功能說明
1. 監測：裝置超聲波傳感器，定期監測房間內的移動物體
2. 報警：蜂鳴器和LED燈，當它偵測到任何潛在的入侵者時，將發出警報聲
3. 巡邏：自主巡邏房間和走廊，以確保區域的安全。如果發現任何異常情況，它將發出警報聲。
4. 遙控：可以透過手機控制機器人，例如啟動或停止巡邏，或直接控制機器人移動到特定位置。

### 設計考量與相關技術
**系統設計考量：**<br>
1. 感測方式: 超聲波、紅外線、光感測或是使用攝像頭
2. 供電方式: 太陽能板或是充電電池
3. 聯網方式:WiFi或BT to 手機
4. 移動方式：輪子

**所需相關技術：**
1.	控制機器人的運動、感應和通訊等功能: Arduino微控制器
2.	偵測障礙物、距離、環境溫度、光線：超聲波感應器、紅外線感應器、攝像頭等
3.	通訊模組： Wi-Fi模組或藍牙模組
4.	軟體開發C++、Python等，可控制機器人運動、感應和通訊等功能的軟體。

### 系統方塊圖
![](https://github.com/ziling819/MCU-project/blob/main/_data/%E5%9C%96%E7%89%871.png?raw=true)
![](<iframe width="1128" height="635" src="https://www.youtube.com/embed/qTxvUu-NBbU" title="MCU微控制器應用-ARM操作步進電機控制線性滑軌" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>)

### 手機藍牙遙控, 或WebUI 遙控(利用手機熱點WiFi連線)
https://user-images.githubusercontent.com/126163590/232207368-21e5e3f6-f348-420e-820a-8ba175787c0a.mp4
https://user-images.githubusercontent.com/126163590/232207377-3c593a41-bd94-4ec0-9e35-4ab81a8a13b3.mp4



### 參考 

<iframe width="1128" height="635" src="https://www.youtube.com/embed/qTxvUu-NBbU" title="MCU微控制器應用-ARM操作步進電機控制線性滑軌" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
---


<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


