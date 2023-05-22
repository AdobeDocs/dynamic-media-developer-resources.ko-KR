---
title: CallToAction.maxloadradius
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 구성 요소 미리 로드 동작을 지정합니다. </p> <p>로 설정된 경우 <span class="codeph"> -1</span> 구성 요소가 초기화되거나 자산이 변경될 때 모든 썸네일들이 동시에 로드됩니다. </p> <p>로 설정된 경우 <span class="codeph"> 0</span> 표시되는 썸네일만 로드됩니다. </p> <p>다음으로 설정 <span class="codeph"><span class="varname"> preloadnbr</span></span> 표시되는 영역 주위에서 사전 로드되는 표시되지 않는 행/열의 수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`-1`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
