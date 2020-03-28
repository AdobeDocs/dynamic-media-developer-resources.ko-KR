---
description: 널
seo-description: 널
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 값 </span></span> </p> </td> 
   <td colname="col2"> <p>데스크톱에서 비디오를 처음 재생하는 데 사용되는 비디오 비트 전송률(초 또는 kbps)을 설정합니다. </p> <p>응용 비디오 세트에 이 비트 전송률 값이 없는 경우 비디오 플레이어는 다음 비트 전송률이 가장 낮은 비디오를 시작합니다. </p> <p>0으로 설정하면 비디오 <span class="codeph"> </span> 플레이어가 가능한 가장 낮은 비트 전송률에서 시작합니다. HTML5 HLS 비디오(Windows 10의 Firefox, Chrome 및 Internet Explorer 11 브라우저)에 대한 기본 지원이 없고 재생 모드가 <span class="codeph"> 자동으로 </span>설정된 경우에만 해당됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
