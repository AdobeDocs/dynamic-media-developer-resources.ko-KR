---
title: VideoScrubber.timepattern
description: VideoScrubber.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0536110e-a885-4fd4-baa8-742fcdba5cc9
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 시간 버블에 표시되는 시간 패턴을 설정합니다. 여기서 <span class="codeph"> h</span>은(는) 시간, <span class="codeph"> m</span>은(는) 분, <span class="codeph"> s</span>은(는) 초입니다. </p> <p>각 시간 단위에 사용되는 문자 수는 단위에 대해 표시할 자릿수를 결정합니다. 숫자가 지정된 자릿수와 맞지 않으면 동등한 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초이면 시간 패턴 <span class="codeph">m:ss</span>은(는) 67:05로 표시됩니다. 지정된 시간 패턴이 <span class="codeph">시간:mm:초</span>인 경우 동일한 시간은 1:07:5로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
