---
description: 재료 서피스 유형입니다. 재료의 서피스 유형을 지정합니다.
seo-description: 재료 서피스 유형입니다. 재료의 서피스 유형을 지정합니다.
seo-title: 유형
solution: Experience Manager
title: 유형
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f107d50-b363-4670-bb02-873677e7bbea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 22%

---


# 유형{#type}

재료 서피스 유형입니다. 재료의 서피스 유형을 지정합니다.

`type=0...19`

<table id="simpletable_482728CD58144E7BBB2912B2F105FDCA"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>알 수 없음, 서버가 기본값을 사용합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>기타 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Natural Wood </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>광택 금속 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p></td> 
  <td class="stentry"> <p>브러시 적용 메탈 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p></td> 
  <td class="stentry"> <p>Antipeed Metal </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p></td> 
  <td class="stentry"> <p>페인트 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p></td> 
  <td class="stentry"> <p>에나멜/라케어 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p></td> 
  <td class="stentry"> <p>벽지 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p></td> 
  <td class="stentry"> <p>플라스틱 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p></td> 
  <td class="stentry"> <p>솔리드 서피스 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p></td> 
  <td class="stentry"> <p>라미네이트 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p></td> 
  <td class="stentry"> <p>비닐 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p></td> 
  <td class="stentry"> <p>세라믹 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p></td> 
  <td class="stentry"> <p>자연석 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p></td> 
  <td class="stentry"> <p>유리 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p></td> 
  <td class="stentry"> <p>미러 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p></td> 
  <td class="stentry"> <p>패브릭 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p></td> 
  <td class="stentry"> <p>순천 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19년 </p></td> 
  <td class="stentry"> <p>카펫 </p></td> 
 </tr> 
</table>

`gloss=` 및 `rough=`과 함께 사용하여 반사 및 광택 효과 동작을 제어합니다. `gloss=` 및 `rough=`이 동일한 경우에도 다른 재질이 다른 효과를 생성합니다.

## 속성 {#section-2345b2508273426295ce8ac46182ea64}

재료 속성. 비네팅에 3D 반사 데이터가 포함되어 있지 않거나 비네팅에서 광택 효과를 사용할 수 없는 경우 무시됩니다.

## 기본값 {#section-0989055fb74a41a3b2f2a47fe7d90a42}

`catalog::Type` 자재가 카탈로그 항목을 기반으로 하는 경우 그렇지 않은 경우 `type=0`. 지정되지 않았거나 `type=0` 인 경우 서버는 대상 객체 및 기타 재료 속성에 따라 적절한 기본값을 선택합니다.

## 참조 {#section-7cf808b0bb3d4b4fbb7b9a850d5a038b}

[광택=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [러프=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)
