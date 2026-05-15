---
title: VideoTime.timepattern
description: VideoTime.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
TQID: 'https://experienceleague.adobe.com/J4UIyQ4XxB0ASY8Yhso0nO45JKrnK9n2hncqqz8JFqs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대에 표시되는 시간 패턴을 설정합니다. 여기서 <span class="codeph"> h</span>은(는) 시간, <span class="codeph"> m</span>은(는) 분, <span class="codeph"> s</span>은(는) 초입니다. </p> <p>각 시간 단위에 사용되는 문자 수는 단위에 대해 표시할 자릿수를 결정합니다. 숫자가 지정된 자릿수와 맞지 않으면 동등한 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초이면 시간 패턴 <span class="codeph">m:ss</span>은(는) 67:05로 표시됩니다. 지정된 시간 패턴이 <span class="codeph">시간:mm:초</span>인 경우 동일한 시간은 1:07:5로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
