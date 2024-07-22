---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`x감도`*[, *`y감도`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> 마우스 끌기 또는 스와이프로 수행되는 수평 및 수직 스핀의 민감도를 제어합니다. </p> <p> <span class="codeph"> xSensitivity</span>은(는) 사용자가 보기의 한 쪽에서 다른 쪽으로 마우스를 수평으로 끌 경우 수행되는 전체 수평 제품 회전 수를 설정합니다. 예를 들어, 3은 사용자가 하나의 전체 드래그 제스처에 대한 3개의 완전한 회전을 본다는 것을 의미한다. </p> <p>마찬가지로 <span class="codeph"> ySensitivity</span>은(는) 수직 스핀의 감도를 제어합니다. 값이 1이면 하나의 전체 수직 드래그 또는 스와이프가 뷰 각도를 최상단 회전 평면에서 최하단(또는 그 반대로)으로 변경함을 의미합니다. </p> <p><span class="codeph"> ySensitivity</span>에 대해 음수 값을 설정하면 수직 스핀의 방향이 반전됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
