---
description: 널
seo-description: 널
seo-title: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
topic: Dynamic media
uuid: 103097e9-7e6d-413c-a6a8-b8a15665348c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`단계 제한`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 단계</span></span> </p> </td> 
   <td colname="col2"> <p> 해상도를 2배로 늘리거나 줄이는 데 필요한 확대/축소 동작 수를 구성합니다. 각 확대/축소 작업에 대한 해상도 변경은 단계당 2^1입니다. 단일 확대/축소 동작을 사용하여 전체 해상도로 확대하려면 <span class="codeph"> 0으로</span> 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 제한</span></span> </p> </td> 
   <td colname="col2"> <p> 전체 해상도 이미지를 기준으로 최대 확대/축소 해상도를 지정합니다. 기본값은 <span class="codeph"> 1.0이며</span>, 전체 해상도를 넘는 확대/축소를 허용하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
