---
description: 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 2e911d35-155e-4afa-aede-52e9d00ae211
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 현재 시스템에서 응용 비디오 재생을 지원하지 않는 경우 응용 비디오 세트에서 재생할 원하는 비디오 비트 전송률(초 또는 kbps)을 지정합니다. </p> <p>구성 요소는 지정된 값에 가장 가까운(하지만 이보다 크지 않은) 비트 전송률로 비디오 스트림을 선택합니다. 응용 비디오 세트의 모든 비디오 스트림의 품질이 지정된 값보다 높은 경우 논리는 가장 낮은 품질로 비트 전송률을 선택합니다. </p> </td> 
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

