---
title: 반복
description: 텍스처 반복 모드. 반복 가능한 질감 재료에 대한 반복 모드를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6cc82742-4ba0-4524-a87b-586539d7fe38
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 16%

---

# 반복{#repeat}

텍스처 반복 모드. 반복 가능한 질감 재료에 대한 반복 모드를 지정합니다.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>곧게 반복해 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>4-way 임의 타일링. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>8방향 무작위 타일링. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>다이아몬드 타일링 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>1/4 낙하 벽지가 매달려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>벽지가 세 번째 드롭으로 걸려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>반쯤 떨어진 벽지가 매달려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>다섯 번째 낙서 벽지가 걸려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>벽지를 거꾸로 매달아 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>무작위로 벽지가 매달려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>무작위 낙하 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>무작위로 가로질러 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>반 옆으로. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>거울 (책 일치). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>표준 무작위화기. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>고주파 무작위화 장치. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>저주파 무작위자. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>수평 무작위화. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>수직 랜더마이저입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Edge 랜더마이저입니다. </p> </td> 
 </tr> 
</table>

무작위 퀼트 모드 (14...18)는 쉽게 반복 가능하지 않은 이미지에서 텍스처를 합성하는 데 사용할 수 있습니다. 알고리즘은 원본 이미지를 기반으로 완전히 무작위 또는 부분적으로 무작위 텍스처를 생성합니다.

## 속성 {#section-262bf540930d4890b678ea00cefe1909}

재질 속성입니다. 단색, 데칼 및 캐비닛 재료에서 무시됩니다.

## 기본값 {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`(자료가 카탈로그 항목을 기반으로 하는 경우), 그렇지 않은 경우 `0`(연속 반복).

## 참조 {#section-ac99113b64654d75a3a86e41db546269}

[catalog::Repeat](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
