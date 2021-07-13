---
description: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,User
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> h</span>이 시간이고, <span class="codeph"> m</span>이 분이고, <span class="codeph"> s</span>가 초인 제어 표시줄에 표시되는 시간의 패턴을 설정합니다. </p> <p>각 시간 단위에 사용되는 글자 수는 단위에 표시할 자릿수를 결정합니다. 숫자가 지정된 자릿수에 맞지 않으면 해당 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초인 경우 시간 패턴 <span class="codeph"> m:ss</span>은 67:05로 표시됩니다. 지정된 시간 패턴이 <span class="codeph"> h:mm:s</span>인 경우 동일한 시간이 1:07:5로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
