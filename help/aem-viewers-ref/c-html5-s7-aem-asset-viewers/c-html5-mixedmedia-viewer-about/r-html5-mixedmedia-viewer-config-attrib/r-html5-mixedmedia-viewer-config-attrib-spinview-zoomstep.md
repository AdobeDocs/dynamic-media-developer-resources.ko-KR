---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: afc2018f-b222-4fd5-b9dc-88655793efd4
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`단계`*[, *`제한`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
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

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
