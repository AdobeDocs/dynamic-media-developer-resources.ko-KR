---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 6%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`단계 제한`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 단계</span></span> </p> </td> 
   <td colname="col2"> <p> 해상도를 2배로 늘리거나 줄이는 데 필요한 숫자 확대 및 축소 작업을 구성합니다. 각 확대/축소 작업에 대한 해상도 변경 사항은 단계당 2^1입니다. 한 번의 확대/축소 작업으로 전체 해상도로 확대하려면 <span class="codeph"> 0</span>으로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 제한</span></span> </p> </td> 
   <td colname="col2"> <p> 전체 해상도 이미지를 기준으로 최대 확대/축소 해상도를 지정합니다. 기본값은 <span class="codeph"> 1.0</span>입니다. 이 경우 전체 해상도를 넘는 확대/축소를 허용하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,1`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
