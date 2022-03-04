---
description: 100% 크기 십진수 객체 너비, 높이 및 두께
solution: Experience Manager
title: 크기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 5%

---

# 크기{#size}

100% 크기 십진수 객체 너비, 높이 및 두께

## 속성 {#section-967bf1112eec4032a91ed0c8a7b10a07}

쉼표로 구분되는 세 개의 실수. 음수는 안 됩니다. 사용하지 않은 값을 0으로 설정합니다. 후행 0은 생략될 수 있습니다.

지정된 크기에 맞게 이미지를 스트레치해야 하는 경우에만 폭과 높이를 모두 지정합니다(종횡비가 변경될 수 있음). 이미지의 비율을 비례적으로 조절하려면 너비나 높이를 설정하십시오. 사용할 너비와 높이를 모두 0으로 설정합니다 `catalog::Resolution`를 눌러 객체 크기를 결정합니다.

두께 값을 제공하여 십진수 객체에 그림자 효과를 추가합니다. 다른 모든 재료에서 무시되는 십진수 재료의 선택 사항입니다.

## 기본값 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0 이는 카탈로그:해상도를 기반으로 십진수 크기를 결정해야 하며 오브젝트에 두께가 없음을 나타냅니다(따라서 그림자 렌더링이 없음).

## 예제 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>decal의 크기는 12x3인치로 강제 설정되며 두께가 없습니다(즉, 그림자 없음). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>디칼은 5인치 너비로, 높이는 이미지의 종횡비에 의해 결정되며, 그림자(drop shadow)는 1인치 두께에 기초하여 렌더링된다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,0.5 </p></td> 
  <td class="stentry"> <p>1/2인치 두께와 높이는 카탈로그로 결정됩니다. </p></td> 
 </tr> 
</table>

## 참조 {#section-31a164e781d14e92bd9d379d3c329e92}

[카탈로그::해상도](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
