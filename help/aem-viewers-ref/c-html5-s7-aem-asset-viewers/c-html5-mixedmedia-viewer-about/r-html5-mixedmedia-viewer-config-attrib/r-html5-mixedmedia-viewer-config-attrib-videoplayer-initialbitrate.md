---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
feature: Dynamic Media Classic,뷰어,SDK/API,혼합 미디어 집합
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>데스크톱에서 비디오를 처음으로 재생하는 데 사용되는 비디오 비트 전송률(초 또는 kbps)을 설정합니다. </p> <p>응용 비디오 집합에 이 비트 전송률 값이 없는 경우 비디오 플레이어는 다음으로 낮은 비트 전송률을 가진 비디오를 시작합니다. </p> <p><span class="codeph"> 0 </span>으로 설정하면 비디오 플레이어가 가능한 가장 낮은 비트 전송률에서 시작합니다. HTML5 HLS 비디오에 대한 기본 지원이 없는 시스템(Windows 10의 Firefox, Chrome 및 Internet Explorer 11 브라우저)과 재생 모드가 <span class="codeph"> auto </span>으로 설정된 경우에만 적용 가능합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
