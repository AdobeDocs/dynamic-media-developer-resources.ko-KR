---
title: VideoPlayer.initialbitrate
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 데스크탑에서 비디오를 처음 재생하는 데 사용되는 비디오 비트율(초당 kbps)을 설정합니다. </p> <p>이 비트율 값이 응용 비디오 세트에 없는 경우 비디오 플레이어는 다음으로 낮은 비트율을 갖는 비디오로 시작합니다. </p> <p><span class="codeph"> 0</span>으로 설정하면 비디오 플레이어가 가능한 가장 낮은 비트율에서 시작됩니다. </p> <p>HTML5 HLS 비디오에 대한 기본 지원이 없는 시스템(예: Windows 10의 Firefox, Chrome 및 Internet Explorer 11 브라우저)과 재생 모드가 자동으로 설정되어 있는 경우에만 적용 가능합니다. </p> </td> 
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
