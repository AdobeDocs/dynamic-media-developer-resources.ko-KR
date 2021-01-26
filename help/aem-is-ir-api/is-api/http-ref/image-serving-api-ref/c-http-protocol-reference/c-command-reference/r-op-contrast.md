---
description: 대비를 조정합니다. 밝기가 50% 이상인 픽셀의 밝기를 높이고 밝기가 50% 미만인 픽셀의 밝기를 줄여 이미지 대비를 조정합니다.
seo-description: 대비를 조정합니다. 밝기가 50% 이상인 픽셀의 밝기를 높이고 밝기가 50% 미만인 픽셀의 밝기를 줄여 이미지 대비를 조정합니다.
seo-title: op_contrast
solution: Experience Manager
title: op_contrast
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---


# op_contrast{#op-contrast}

대비를 조정합니다. 밝기가 50% 이상인 픽셀의 밝기를 높이고 밝기가 50% 미만인 픽셀의 밝기를 줄여 이미지 대비를 조정합니다.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>대비 조정 비율(-100...100 int). </p></td> 
 </tr> 
</table>

## 속성 {#section-d319ed55057344eab0a3c93f720acdbf}

레이어 명령. `layer=comp`인 경우 현재 레이어나 합성 이미지에 적용됩니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`을 선택합니다. CMYK 이미지 또는 레이어는 작업이 적용되기 전에 RGB로 변환됩니다.

## 예 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

고품질의 이미지 레이어의 대비 및 선명도를 줄여 저품질의 배경 사진에 시각적으로 일치시킵니다.

… `&op_blur=3&op_contrast=-12&`

향후 릴리스는 고정된 50% 밝기가 아니라 이미지의 중간값을 사용할 수 있습니다.
