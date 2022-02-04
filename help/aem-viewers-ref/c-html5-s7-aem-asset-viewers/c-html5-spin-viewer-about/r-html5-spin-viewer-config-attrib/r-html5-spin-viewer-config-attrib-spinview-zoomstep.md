---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`단계`*[, *`제한`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 단계</span></span> </p> </td> 
   <td colname="col2"> <p> 해상도를 두 배수로 늘리거나 줄이는 데 필요한 확대/축소 작업 수를 구성합니다. 각 확대/축소 작업에 대한 해상도 변경은 단계당 2^1입니다. 을 로 설정합니다. <span class="codeph"> 0</span> 한 번의 확대/축소 작업으로 전체 해상도로 확대/축소합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 제한</span></span> </p> </td> 
   <td colname="col2"> <p> 전체 해상도 이미지를 기준으로 최대 확대/축소 해상도를 지정합니다. 기본값은 입니다. <span class="codeph"> 1.0</span>- 전체 해상도를 넘어 확대/축소를 허용하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-924163cb2f6542499f49894becef7fb5}

선택 사항입니다.

## 기본값 {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## 예 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
