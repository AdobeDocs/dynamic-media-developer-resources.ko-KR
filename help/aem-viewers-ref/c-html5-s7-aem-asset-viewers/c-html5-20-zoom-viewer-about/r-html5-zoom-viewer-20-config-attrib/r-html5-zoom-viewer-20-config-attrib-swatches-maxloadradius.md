---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: df9d5be4-d1e1-4b72-a7e7-0f3611278d2a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 5%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>구성 요소 미리 로드 동작을 지정합니다. <span class="codeph"> -1</span>(으)로 설정하면 구성 요소가 초기화되거나 자산이 변경될 때 모든 견본들이 동시에 로드됩니다. </p> <p><span class="codeph"> 0</span>(으)로 설정하면 보이는 견본만 로드됩니다. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>은(는) 표시되는 영역 주위에서 사전 로드되는 표시되지 않는 행/열의 수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=-1`
