---
title: 자르기
description: 이미지 자르기. 전체 해상도 소스 이미지 또는 마스크 이미지를 기준으로 픽셀 단위 또는 표준화된 사각형 자르기 영역을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# 자르기{#crop}

이미지 자르기. 전체 해상도 소스 이미지 또는 마스크 이미지를 기준으로 픽셀 단위 또는 표준화된 사각형 자르기 영역을 지정합니다.

`crop= *`주역`*, *`크기`*`

`cropN= *`coordN`*, *`크기 N`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 주역</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리에서 자르기 rect의 왼쪽 위(int, int)까지의 픽셀 오프셋. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 상단에서 자르기 rect의 왼쪽 상단까지 정규화된 오프셋(실수, 실수). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 크기</span></span> </p></td> 
  <td class="stentry"> <p>자르기 rect 픽셀 단위 크기입니다(int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 크기 N</span></span> </p></td> 
  <td class="stentry"> <p>소스 이미지의 크기를 기준으로 자르기 rect의 표준화된 크기입니다(실수, 실수). </p></td> 
 </tr> 
</table>

이미지 너비, 높이보다 큰 음수 x, y 값 및/또는 너비, 높이 값을 지정하여 이미지를 경계 이상으로 확장하는 데 사용할 수도 있습니다. 이 경우 확장된 영역은 완전히 투명합니다(그렇지 않으면 `bgColor=` 을(를) 지정했습니다.

## 속성 {#section-632e0405bb9940679b5f8b1c10e0902e}

소스 이미지/마스크 속성. 다음과 같은 경우 레이어 0 소스 이미지에 적용됩니다. `layer=comp`. 소스 이미지 또는 마스크와 연관되지 않은 레이어에서 무시됩니다.

## 기본값 {#section-41f62d386c664f77952bc22e7286bb88}

전체 이미지( `cropN=0,0,1,1`).

## 예제 {#section-2c99b481c0a04321979a3b522aa295d1}

**왼쪽의 10%와 오른쪽의 10%를 자르세요.**

`…&cropN=0.1,0,0.8,1&…`

**이미지의 아래쪽 가장자리에서 20%를 자릅니다.**

`…&cropN=0,0,1,0.8&…`

## 참조 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[자르기 경로](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [앵커=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
