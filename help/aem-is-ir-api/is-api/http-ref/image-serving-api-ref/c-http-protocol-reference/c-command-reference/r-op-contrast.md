---
title: op_contrast
description: 대비를 조정합니다. 밝기 비율이 50%를 초과하는 픽셀의 밝기를 높이고 밝기 비율이 50%를 초과하는 픽셀의 밝기를 줄여 이미지 대비를 조정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
TQID: 'https://experienceleague.adobe.com/Ob098G38TFXX0HzB3JQOCcdD9ZnrYWrMum6XEQSmGRU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 1%

---

# op_contrast{#op-contrast}

대비를 조정합니다. 밝기 비율이 50%를 초과하는 픽셀의 밝기를 높이고 밝기 비율이 50%를 초과하는 픽셀의 밝기를 줄여 이미지 대비를 조정합니다.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>대비 조정 비율(-100...100 int) </p></td> 
 </tr> 
</table>

## 속성 {#section-d319ed55057344eab0a3c93f720acdbf}

레이어 명령. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`(대비가 변경되지 않음). CMYK 이미지 또는 레이어는 작업을 적용하기 전에 RGB으로 변환됩니다.

## 예 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

고품질 이미지 레이어의 대비 및 선명도를 낮춰 저품질 배경 사진과 시각적으로 일치시킵니다.

... `&op_blur=3&op_contrast=-12&`

향후 릴리스에서는 고정된 50% 밝기가 아닌 이미지의 중간 밝기를 사용할 수 있습니다.
