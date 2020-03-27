---
description: 널
seo-description: 널
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: 6034dc22-c1d4-4a37-93de-42a88b99234a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 시간 버블에 표시되는 시간의 패턴을 설정합니다. 여기서 <span class="codeph"> h</span> 는 시간, <span class="codeph"> m</span><span class="codeph"> 은 분,</span> s는 초입니다. </p> <p>각 시간 단위에 사용되는 문자 수는 해당 단위에 대해 표시할 자릿수를 결정합니다. 해당 숫자가 지정된 숫자에 맞지 않으면 해당 값이 다음 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초인 경우 시간 패턴 <span class="codeph"> m:ss</span> 는 67:05로 표시됩니다. 주어진 시간 패턴이 <span class="codeph"> h:mm:s인 경우 동일한 시간이 1:07:5로 표시됩니다</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
