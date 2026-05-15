---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
TQID: 'https://experienceleague.adobe.com/7EPprL4pjlCHtiIfz2-6pmWvwfV3DZINE4wjjkkRXNM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`단계`*[, *`제한`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">단계</span></span> </p> </td> 
   <td colname="col2"> <p> 해상도를 2배율로 증가/감소시키는 데 필요한 확대/축소 동작 수를 구성합니다. 각 확대/축소 동작에 대한 해상도 변경은 단계당 2^1입니다. 한 번의 확대/축소 작업으로 전체 해상도로 확대/축소하려면 <span class="codeph"> 0</span>(으)로 설정하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 제한</span></span> </p> </td> 
   <td colname="col2"> <p> 전체 해상도 이미지를 기준으로 최대 확대/축소 해상도를 지정합니다. 기본값은 <span class="codeph"> 1.0</span>이며, 최대 해상도 범위를 넘지 않게 확대/축소를 제한합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-924163cb2f6542499f49894becef7fb5}

선택적.

## 기본값 {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## 예 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
