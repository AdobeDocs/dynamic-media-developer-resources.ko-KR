---
title: SmartCropVideoPlayer.progressivebitrate
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 현재 시스템이 응용 비디오 재생을 지원하지 않는 경우 응용 비디오 세트에서 재생할 원하는 비디오 비트 전송률(초당 킬로비트 또는 Kbps)을 지정합니다. </p> <p>구성 요소는 지정된 값에 가장 가까운(하지만 초과하지 않는) 비트율을 사용하여 비디오 스트림을 선택합니다. 응용 비디오 세트의 모든 비디오 스트림의 품질이 지정된 값보다 높은 경우 논리가 가장 낮은 품질을 사용하여 비트율을 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
