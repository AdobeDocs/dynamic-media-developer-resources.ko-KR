---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>데스크탑에서 비디오를 처음 재생하는 데 사용되는 비디오 비트율(초 또는 kbps)을 설정합니다. </p> <p>이 비트율 값이 응용 비디오 세트에 없는 경우 비디오 플레이어에서 다음으로 낮은 비트율을 갖는 비디오를 시작합니다. </p> <p><span class="codeph"> 0 </span> 로 설정하면 비디오 플레이어가 가능한 가장 낮은 비트율에서 시작됩니다. HTML5 HLS 비디오(Windows 10의 Firefox, Chrome 및 Internet Explorer 11 브라우저)에 대한 기본 지원이 없고 재생 모드가 <span class="codeph"> auto </span>로 설정된 경우에만 적용 가능합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
