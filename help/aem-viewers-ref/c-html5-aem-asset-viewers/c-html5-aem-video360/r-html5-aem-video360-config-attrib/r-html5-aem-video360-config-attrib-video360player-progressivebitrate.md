---
title: Video360Player.progressivebitrate
description: Video360 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360 뷰어에 대한 구성 속성입니다.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`값`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 값</span> </p> </td> 
   <td colname="col2"> <p> 현재 시스템이 응용 비디오 재생을 지원하지 않을 것에 대비하여 응용 비디오 세트에서 재생할 원하는 비디오 비트 전송률(초당 킬로비트 또는 kbps)을 지정합니다. </p> <p>구성 요소는 지정된 값과 가장 가까운 가능한(하지만 초과하지는 않는) 비트율의 비디오 스트림을 선택하게 됩니다. 응용 비디오 세트의 모든 비디오 스트림의 품질이 지정된 값보다 높은 경우 논리에서는 가장 낮은 품질을 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
