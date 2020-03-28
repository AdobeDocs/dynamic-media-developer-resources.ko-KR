---
description: 널
seo-description: 널
seo-title: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
topic: Dynamic media
uuid: 948b154a-250c-41a8-967b-d199ddb6e5e1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`단계 제한`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 단계</span></span> </p> </td> 
   <td colname="col2"> <p> 해상도를 2배로 늘리거나 줄이는 데 필요한 확대 및 축소 동작 수를 구성합니다. 각 확대/축소 작업에 대한 해상도 변경은 단계당 2^1입니다. 단일 확대/축소 동작을 사용하여 전체 해상도로 확대하려면 <span class="codeph"> 0으로</span> 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 제한</span></span> </p> </td> 
   <td colname="col2"> <p> 전체 해상도 이미지를 기준으로 최대 확대/축소 해상도를 지정합니다. 기본값은 <span class="codeph"> 1.0이며</span>, 전체 해상도를 넘는 확대/축소를 허용하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-50bcd15223174bb79ce08b31ea03d682}

선택 사항입니다.

## 기본값 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## 예 {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
