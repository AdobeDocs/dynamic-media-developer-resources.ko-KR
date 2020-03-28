---
description: 이미지 자르기를 참조하십시오. 전체 해상도 소스 이미지 또는 마스크 이미지를 기준으로 픽셀 단위로 표현되거나 표준화된 사각형 자르기 영역을 지정합니다.
seo-description: 이미지 자르기를 참조하십시오. 전체 해상도 소스 이미지 또는 마스크 이미지를 기준으로 픽셀 단위로 표현되거나 표준화된 사각형 자르기 영역을 지정합니다.
seo-title: 자르기
solution: Experience Manager
title: 자르기
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 자르기{#crop}

이미지 자르기를 참조하십시오. 전체 해상도 소스 이미지 또는 마스크 이미지를 기준으로 픽셀 단위로 표현되거나 표준화된 사각형 자르기 영역을 지정합니다.

`crop= *``*, *`표준 크기`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 코드</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리에서 왼쪽 위 모서리까지의 픽셀 오프셋(int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 상단에서 왼쪽 상단으로 정규화된 오프셋(실제, 실제) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 크기 <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>자르기 사각형 크기(픽셀 단위: int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 크기 <span class="varname"> N</span></span> </p></td> 
  <td class="stentry"> <p>소스 이미지 크기(실제, 실제)를 기준으로 하는 자르기의 정규화된 크기 </p></td> 
 </tr> 
</table>

이미지 폭, 높이보다 큰 음수 x, y 값 및/또는 폭, 높이 값을 지정하여 이미지를 경계 밖으로 확장하는 데에도 사용할 수 있습니다. 이 경우 확장 영역은 완전히 투명합니다(지정하지 `bgColor=` 않은 경우).

## 속성 {#section-632e0405bb9940679b5f8b1c10e0902e}

소스 이미지/마스크 속성입니다. Apples to the layer 0 source image if `layer=comp`. 소스 이미지 또는 마스크와 연결되지 않은 레이어에서 무시됩니다.

## 기본값 {#section-41f62d386c664f77952bc22e7286bb88}

전체 이미지( `cropN=0,0,1,1`).

## 예제 {#section-2c99b481c0a04321979a3b522aa295d1}

**왼쪽 10%, 오른쪽 10% 자르기:**

`…&cropN=0.1,0,0.8,1&…`

**이미지의 아래쪽 가장자리를 20% 잘라냅니다.**

`…&cropN=0,0,1,0.8&…`

## 참조 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
