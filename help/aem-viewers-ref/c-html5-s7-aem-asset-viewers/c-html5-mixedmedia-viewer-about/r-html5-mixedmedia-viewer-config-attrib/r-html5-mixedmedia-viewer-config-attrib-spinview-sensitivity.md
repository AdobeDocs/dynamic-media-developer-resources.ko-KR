---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`민감도 민감도`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> 마우스로 끌거나 밀면서 수행되는 수평 및 수직 스핀 민감도를 제어합니다. </p> <p> <span class="codeph"> </span> 사용자가 마우스를 보기의 한 쪽에서 다른 면으로 가로로 드래그하면 가로 전체 제품 회전의 수를 감지합니다. 예를 들어, 3은 사용자가 하나의 전체 드래그 제스처에 대해 세 개의 전체 회전을 보았다는 것을 의미합니다. </p> <p>마찬가지로 <span class="codeph"> ySensitivity</span>는 수직 스핀의 민감도를 제어합니다. 값이 1이면 가장 높은 스핀 평면에서 가장 아래쪽(또는 그 반대)으로 전체 수직 드래그 또는 스와이프가 뷰 각도를 변경함을 의미합니다. </p> <p><span class="codeph"> ySensitivity</span>에 음수 값을 설정하면 수직 스핀 방향이 반전됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
