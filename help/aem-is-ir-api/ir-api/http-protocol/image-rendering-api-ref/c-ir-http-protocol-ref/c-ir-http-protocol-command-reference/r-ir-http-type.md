---
title: 유형
description: 재료 서피스 유형. 재료의 서피스 유형을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 333b8954-e256-4ba1-8055-c4d625470673
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 17%

---

# 유형{#type}

재료 서피스 유형. 재료의 서피스 유형을 지정합니다.

`type=0...19`

<table id="simpletable_482728CD58144E7BBB2912B2F105FDCA"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>알 수 없음, 서버에서 기본값 사용 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>기타 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>천연 목재 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>연마된 금속 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p></td> 
  <td class="stentry"> <p>브러시드 메탈 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p></td> 
  <td class="stentry"> <p>오래된 금속 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p></td> 
  <td class="stentry"> <p>페인트 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p></td> 
  <td class="stentry"> <p>에나멜/래커 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p></td> 
  <td class="stentry"> <p>배경 무늬 </p></td> 
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
  <td class="stentry"> <p>쉬어 패브릭 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p></td> 
  <td class="stentry"> <p>카펫 </p></td> 
 </tr> 
</table>

반사 및 광택 효과 동작을 제어하기 위해 `gloss=` 및 `rough=`과(와) 함께 사용됩니다. `gloss=`과(와) `rough=`이(가) 동일한 경우에도 다른 재료가 다른 효과를 냅니다.

## 속성 {#section-2345b2508273426295ce8ac46182ea64}

재질 속성입니다. 비네팅에 3D 반사 데이터가 포함되지 않았거나 비네팅에서 광택 효과가 비활성화된 경우에는 무시됩니다.

## 기본값 {#section-0989055fb74a41a3b2f2a47fe7d90a42}

`catalog::Type` 자료가 카탈로그 항목을 기반으로 하는 경우. 그렇지 않으면 `type=0`입니다. 지정하지 않거나 `type=0`인 경우 서버는 대상 개체 및 기타 재질 특성에 따라 적절한 기본값을 선택합니다.

## 참조 {#section-7cf808b0bb3d4b4fbb7b9a850d5a038b}

[광택=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [황삭=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)
