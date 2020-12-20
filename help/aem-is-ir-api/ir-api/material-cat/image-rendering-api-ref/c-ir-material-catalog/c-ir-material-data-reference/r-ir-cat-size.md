---
description: 100% 크기 decal material 객체의 폭, 높이 및 두께입니다.
seo-description: 100% 크기 decal material 객체의 폭, 높이 및 두께입니다.
seo-title: 크기
solution: Experience Manager
title: 크기
topic: Scene7 Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 5%

---


# 크기{#size}

100% 크기 decal material 객체의 폭, 높이 및 두께입니다.

## 속성 {#section-967bf1112eec4032a91ed0c8a7b10a07}

3개의 실수는 쉼표로 구분됩니다. 음수여야 합니다. 사용하지 않은 값을 0으로 설정합니다. 후행 0은 생략될 수 있습니다.

지정된 크기에 맞게 이미지를 스트레치해야 하는 경우에만 폭과 높이를 모두 지정합니다(종횡비가 변경될 수 있음). 너비나 높이를 설정하여 이미지의 비율을 비례적으로 조정합니다. `catalog::Resolution`을 사용하여 개체 크기를 결정하려면 폭과 높이를 모두 0으로 설정합니다.

decal 객체에 그림자를 추가하려면 두께 값을 제공합니다. 다른 모든 재질에서 무시되는 디폴트 재질의 선택 사항입니다.

## 기본값 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0 이것은 decal 크기를 카탈로그::Resolution에 따라 결정하고 개체에 두께가 없으므로 그림자가 렌더링되지 않음을 나타냅니다.

## 예제 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>디캘은 크기가 12x3인치로 제한되며 두께가 없습니다(즉, 그림자 없음). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>디칼은 폭이 5인치, 높이는 이미지의 종횡비에 의해 결정되고 그림자는 1인치 두께를 기준으로 렌더링됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,0.5 </p></td> 
  <td class="stentry"> <p>디폴트 너비와 높이는 [해상도]로 결정되며 1/2 인치 두께입니다. </p></td> 
 </tr> 
</table>

## 참조 {#section-31a164e781d14e92bd9d379d3c329e92}

[카탈로그::해상도](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
