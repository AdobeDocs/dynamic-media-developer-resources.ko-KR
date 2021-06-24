---
description: 이미지 자르기. 전체 해상도 소스 이미지나 마스크 이미지에 대해 픽셀 단위로 표시되거나 정규화된 사각형 자르기 영역을 지정합니다.
solution: Experience Manager
title: 자르기
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---

# 자르기{#crop}

이미지 자르기. 전체 해상도 소스 이미지나 마스크 이미지에 대해 픽셀 단위로 표시되거나 정규화된 사각형 자르기 영역을 지정합니다.

`crop= *``*, *`coordsize`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 코드</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리에서 자르기 레트의 왼쪽 위(int, int)까지 픽셀 오프셋입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위에서 자르기 레트의 왼쪽 상단까지 정규화된 오프셋(실제, 실제)입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 크기</span></span> </p></td> 
  <td class="stentry"> <p>자르기 레코드 크기(픽셀 단위)입니다(int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 크기에 상대적인 자르기 작업의 정규화된 크기(실제, 실제)입니다. </p></td> 
 </tr> 
</table>

또한 음수 x, y 값 및/또는 폭과 이미지 너비, 높이보다 큰 높이 값을 지정하여 이미지를 해당 경계 이상으로 확장하는 데 사용할 수도 있습니다. 이 경우 확장 영역은 완전히 투명합니다( `bgColor=`을 지정하지 않은 경우).

## 속성 {#section-632e0405bb9940679b5f8b1c10e0902e}

소스 이미지/마스크 속성입니다. `layer=comp`인 경우 레이어 0 소스 이미지에 적용됩니다. 소스 이미지나 마스크와 연관되지 않은 레이어에서 무시됩니다.

## 기본값 {#section-41f62d386c664f77952bc22e7286bb88}

전체 이미지( `cropN=0,0,1,1`).

## 예제 {#section-2c99b481c0a04321979a3b522aa295d1}

**자르기는 왼쪽에서 10%, 오른쪽은 10%입니다.**

`…&cropN=0.1,0,0.8,1&…`

**이미지 하단 가장자리에서 20% 자르기:**

`…&cropN=0,0,1,0.8&…`

## 참조 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [cropPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
