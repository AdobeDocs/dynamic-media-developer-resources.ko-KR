---
title: 크기
description: 데칼 크기. 데칼 재질 개체의 너비, 높이 및 두께입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 4%

---

# 크기{#size}

데칼 크기. 데칼 재질 개체의 너비, 높이 및 두께입니다.

## 속성 {#section-967bf1112eec4032a91ed0c8a7b10a07}

쉼표로 구분된 실수 세 개. 음수가 아니어야 합니다. 사용하지 않는 값을 0으로 설정합니다. 후행 0은 생략할 수 있습니다.

이미지를 지정된 크기에 맞게 늘려야 하는 경우에만 너비와 높이를 모두 지정합니다(종횡비가 변경될 수 있음). 이미지의 비율을 비례적으로 조절하려면 너비 또는 높이를 설정하십시오. 을 사용하려면 너비와 높이를 모두 0으로 설정하십시오 `catalog::Resolution`개체 크기를 결정합니다.

decal 객체에 그림자를 추가하려면 두께 값을 입력합니다. 데칼 소재는 선택 사항이며 다른 모든 소재는 무시됩니다.

## 기본값 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. 이는 decal 크기가 catalog::Resolution에 따라 결정되고 오브젝트에 두께가 없음을 나타냅니다(따라서 그림자가 렌더링되지 않음).

## 예제 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>데칼은 크기가 12x3 인치로 강제 설정되고 두께가 없습니다(즉, 그림자 없음). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>데칼의 너비는 5인치이고, 높이는 이미지의 종횡비에 의해 결정되며, 그림자는 1인치 두께를 기준으로 렌더링됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>데칼 너비와 높이는 catalog::Resolution에 따라 결정되며 두께는 ½ 인치입니다. </p></td> 
 </tr> 
</table>

## 참조 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
