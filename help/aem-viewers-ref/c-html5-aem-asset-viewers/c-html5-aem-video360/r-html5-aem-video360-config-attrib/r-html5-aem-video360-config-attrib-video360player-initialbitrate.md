---
description: Video360 뷰어에 대한 구성 속성입니다.
seo-description: Video360 뷰어에 대한 구성 속성입니다.
seo-title: Video360Player.initialbitrate
solution: Experience Manager
title: Video360Player.initialbitrate
topic: Dynamic media
uuid: a23fa941-6dd2-41c0-aca9-06f0cdb027b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 8%

---


# Video360Player.initialbitrate{#video-player-initialbitrate}

Video360 뷰어에 대한 구성 속성입니다.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 데스크톱에서 비디오를 처음으로 재생하는 데 사용되는 비디오 비트 전송률(초당 kbits 또는 kbps)을 설정합니다. </p> <p>응용 비디오 집합에 이 비트 전송률 값이 없는 경우 비디오 플레이어는 다음 비트 전송률이 낮은 비디오로 시작합니다. </p> <p><span class="codeph"> 0</span>으로 설정하면 비디오 플레이어가 가능한 가장 낮은 비트 전송률에서 시작합니다. </p> <p>HTML5 HLS 비디오에 대한 기본 지원이 없는 시스템(Windows 10의 Firefox, Chrome 및 Internet Explorer 11 브라우저 등)과 재생 모드가 [자동]으로 설정된 경우에만 해당됩니다. </p> </td> 
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

