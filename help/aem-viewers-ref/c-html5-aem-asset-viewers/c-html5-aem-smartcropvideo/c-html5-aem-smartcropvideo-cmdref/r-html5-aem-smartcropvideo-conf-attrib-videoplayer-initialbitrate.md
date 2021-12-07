---
title: SmartCropVideoPlayer.initialbitrate
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

비디오 뷰어에 대한 구성 속성입니다.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>데스크탑에서 비디오를 처음 재생하는 데 사용되는 비디오 비트율(초 또는 Kbps)을 설정합니다. </p> <p>이 비트율 값이 응용 비디오 세트에 없는 경우 비디오 플레이어에서 다음으로 낮은 비트율을 갖는 비디오를 시작합니다. </p> <p>로 설정된 경우 <span class="codeph"> 0 </span>: 비디오 플레이어가 가능한 가장 낮은 비트율에서 시작됩니다. HTML5 HLS 비디오(Windows 10의 Firefox, Chrome 및 Internet Explorer 11 브라우저)에 대한 기본 지원이 없고 재생 모드가 로 설정된 경우에만 적용 가능합니다 <span class="codeph"> 자동 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
