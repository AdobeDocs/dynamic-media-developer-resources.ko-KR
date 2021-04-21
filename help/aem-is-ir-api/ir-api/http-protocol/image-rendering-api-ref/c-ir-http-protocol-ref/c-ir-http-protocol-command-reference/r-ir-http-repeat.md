---
description: 텍스처 반복 모드. 반복 가능한 텍스처 재질에 대한 반복 모드를 지정합니다.
solution: Experience Manager
title: 반복
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 16%

---


# 반복{#repeat}

텍스처 반복 모드. 반복 가능한 텍스처 재질에 대한 반복 모드를 지정합니다.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>반복해 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>4방향 임의 타일링 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>8방향 임의 타일링 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>다이아몬드 타일링. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>1/4드롭 배경 무늬 표시 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>셋드롭 벽지가 걸려 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>반쪽짜리 벽지가 걸려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>5번째 벽지가 걸려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>배경 무늬 반전. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>무작위 벽지가 멈춥니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>임의 드롭. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>무작위 범위 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>반쪽입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>미러(북일치). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>표준 무작위 지정. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>높은 주파수 무작위 추출기. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>낮은 주파수 무작위 추출기. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>수평 무작위 기호 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>수직 무작위 기호 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19년 </p> </td> 
  <td class="stentry"> <p>가장자리 임의화 프로그램. </p> </td> 
 </tr> 
</table>

임의 퀼트 모드(14...18)를 사용하여 쉽게 반복할 수 없는 이미지의 텍스처를 합성할 수 있습니다.알고리즘은 원본 이미지를 기반으로 임의 텍스처나 부분적으로 임의 텍스처를 만듭니다.

## 속성 {#section-262bf540930d4890b678ea00cefe1909}

재료 속성. 단색, 십자 및 캐비닛 재질로 무시됩니다.

## 기본값 {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, 자료가 카탈로그 항목을 기반으로 하는 경우, 그렇지 않은 경우  `0` (직선 반복)

## 참조 {#section-ac99113b64654d75a3a86e41db546269}

[카탈로그::반복](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
