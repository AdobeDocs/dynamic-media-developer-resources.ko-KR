---
title: VideoPlayer.progressivebitrate
description: VideoPlayer.progressivebitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: b156d3f4-c4d3-45fe-b3d3-b7ed38f6eb4d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`값`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 값</span></span> </p> </td> 
   <td colname="col2"> <p> 현재 시스템이 응용 비디오 재생을 지원하지 않을 것에 대비하여 응용 비디오 세트에서 재생할 원하는 비디오 비트 전송률(초당 킬로비트 또는 kbps)을 지정합니다. </p> <p>구성 요소는 지정된 값과 가장 가까운 가능한(하지만 초과하지는 않는) 비트율의 비디오 스트림을 선택하게 됩니다. 응용 비디오 세트의 모든 비디오 스트림의 품질이 지정된 값보다 높은 경우 논리에서는 가장 낮은 품질을 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
