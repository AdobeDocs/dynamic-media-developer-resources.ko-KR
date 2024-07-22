---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`단계`*[, *`제한`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 단계</span> </span> </p> </td> 
   <td colname="col2"> <p> 해상도를 2배율로 증가/감소시키는 데 필요한 확대/축소 동작 수를 구성합니다. 각 확대/축소 동작에 대한 해상도 변경은 단계당 2^1입니다. 한 번의 확대/축소 작업으로 전체 해상도로 확대/축소하려면 <span class="codeph"> 0</span>(으)로 설정하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 제한</span> </span> </p> </td> 
   <td colname="col2"> <p> 전체 해상도 이미지를 기준으로 최대 확대/축소 해상도를 지정합니다. 기본값은 <span class="codeph"> 1.0</span>이며, 최대 해상도 범위를 넘지 않게 확대/축소를 제한합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-50bcd15223174bb79ce08b31ea03d682}

선택적.

## 기본값 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## 예 {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
