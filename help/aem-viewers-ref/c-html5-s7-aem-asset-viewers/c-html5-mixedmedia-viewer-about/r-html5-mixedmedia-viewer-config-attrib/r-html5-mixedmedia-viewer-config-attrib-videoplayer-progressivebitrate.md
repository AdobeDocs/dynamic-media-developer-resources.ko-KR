---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 94de31cd-2b4e-4247-b181-26666767f065
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> 현재 시스템에서 응용 비디오 재생을 지원하지 않는 경우 응용 비디오 세트에서 재생할 원하는 비디오 비트 전송률(초 또는 kbps)을 지정합니다. </p> <p>구성 요소는 지정된 값에 가장 근접한(초과) 비트 전송률을 사용하여 비디오 스트림을 선택합니다. 응용 비디오 집합의 모든 비디오 스트림의 품질이 지정된 값보다 높은 경우 가장 낮은 품질로 비트 전송률을 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
