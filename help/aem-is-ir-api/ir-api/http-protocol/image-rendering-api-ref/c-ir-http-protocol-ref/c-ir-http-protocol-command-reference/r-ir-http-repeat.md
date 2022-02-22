---
title: 반복
description: 텍스처 반복 모드. 반복 가능한 텍스쳐 재질에 대한 반복 모드를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6cc82742-4ba0-4524-a87b-586539d7fe38
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 16%

---

# 반복{#repeat}

텍스처 반복 모드. 반복 가능한 텍스쳐 재질에 대한 반복 모드를 지정합니다.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>연속 반복. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>4방향 임의 타일링. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>8방향 임의 타일링. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>다이아몬드 타일링. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>1/4방울 무늬 벽지가 걸려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>3단 벽지가 걸려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>반쪽무늬 벽지가 걸려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>다섯번째 벽지가 걸려 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>벽지가 거꾸로 걸려요 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>난벽지가 걸려있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>임의 드롭. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>무작위 반대입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>반쪽이요 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>미러(북 일치). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>표준 무작위 지정 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>빈도가 높은 랜덤라이저. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>빈도가 낮은 무작위 분류기입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>수평 임의화. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>수직 무작위 지정 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Edge Randomizer. </p> </td> 
 </tr> 
</table>

무작위 퀼트 모드(14... 18)는 쉽게 반복할 수 없는 영상의 텍스처를 합성하는 데 사용될 수 있다. 알고리즘은 원래 이미지를 기반으로 완전히 임의 또는 부분적으로 임의 텍스처를 생성합니다.

## 속성 {#section-262bf540930d4890b678ea00cefe1909}

재료 속성입니다. 고색, 십자 및 캐비닛 자료에 의해 무시됩니다.

## 기본값 {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, 자료가 카탈로그 항목을 기반으로 하는 경우, 그렇지 않으면 `0` (연속 반복).

## 참조 {#section-ac99113b64654d75a3a86e41db546269}

[카탈로그::반복](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
