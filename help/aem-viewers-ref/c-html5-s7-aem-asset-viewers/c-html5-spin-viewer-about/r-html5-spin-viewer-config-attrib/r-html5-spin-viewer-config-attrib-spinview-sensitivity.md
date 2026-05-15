---
title: SpinView.민감도
description: SpinView.민감도
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
TQID: 'https://experienceleague.adobe.com/B19x2Bn3GNq8YFUo-0HiSbyBQ4qrMcONvRSN1tNqOg0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# SpinView.민감도{#spinview-sensitivity}

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
