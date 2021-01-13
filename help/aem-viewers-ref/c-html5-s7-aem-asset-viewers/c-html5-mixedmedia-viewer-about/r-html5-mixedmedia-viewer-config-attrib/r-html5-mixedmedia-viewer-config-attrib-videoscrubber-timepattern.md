---
description: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: 6034dc22-c1d4-4a37-93de-42a88b99234a
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 시간 버블에 표시되는 시간의 패턴을 설정합니다. 여기서 <span class="codeph"> h</span>은 시간, <span class="codeph"> m</span>은 분, <span class="codeph"> s</span>는 초입니다. </p> <p>각 시간 단위에 사용된 문자 수는 해당 단위에 대해 표시할 자릿수를 결정합니다. 숫자가 지정된 숫자에 맞지 않을 경우, 해당 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초이면 시간 패턴 <span class="codeph"> m:ss</span>이 67:05로 표시됩니다. 지정된 시간 패턴이 <span class="codeph"> h:mm:s</span>인 경우 같은 시간이 1:07:5으로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
