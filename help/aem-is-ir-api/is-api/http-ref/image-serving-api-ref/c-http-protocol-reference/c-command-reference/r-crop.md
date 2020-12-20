---
description: 이미지 자르기를 참조하십시오. 전체 해상도 소스 이미지 또는 마스크 이미지를 기준으로 픽셀 단위로 표시되거나 표준화된 사각형 자르기 영역을 지정합니다.
seo-description: 이미지 자르기를 참조하십시오. 전체 해상도 소스 이미지 또는 마스크 이미지를 기준으로 픽셀 단위로 표시되거나 표준화된 사각형 자르기 영역을 지정합니다.
seo-title: 자르기
solution: Experience Manager
title: 자르기
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 3%

---


# 자르기{#crop}

이미지 자르기를 참조하십시오. 전체 해상도 소스 이미지 또는 마스크 이미지를 기준으로 픽셀 단위로 표시되거나 표준화된 사각형 자르기 영역을 지정합니다.

`crop= *``*, *`조정 크기`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리에서 자르기 사각형 왼쪽 위(int, int)까지 픽셀 오프셋입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위에서 자르기 사각형 왼쪽 위(실제)까지 정규화된 오프셋입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 크기</span></span> </p></td> 
  <td class="stentry"> <p>자르기 사각형 크기(픽셀 단위)(int, int)입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>소스 이미지 크기(실제, 실제)를 기준으로 자르기 크기의 정규화된 크기가 다시 표시됩니다. </p></td> 
 </tr> 
</table>

이미지 폭, 높이보다 큰 음수 x, y 값 및/또는 너비, 높이 값을 지정하여 이미지를 해당 경계 너머로 확장하도록 사용할 수도 있습니다. 이 경우 확장 영역은 완전히 투명하게 표시됩니다(`bgColor=`이 지정되지 않은 경우).

## 속성 {#section-632e0405bb9940679b5f8b1c10e0902e}

소스 이미지/마스크 속성입니다. `layer=comp`인 경우 레이어 0 소스 이미지에 적용됩니다. 소스 이미지 또는 마스크와 연결되지 않은 레이어에서 무시됩니다.

## 기본값 {#section-41f62d386c664f77952bc22e7286bb88}

전체 이미지( `cropN=0,0,1,1`).

## 예제 {#section-2c99b481c0a04321979a3b522aa295d1}

**왼쪽에서 10%, 오른쪽에서 10% 자르기:**

`…&cropN=0.1,0,0.8,1&…`

**이미지의 아래쪽 가장자리를 20% 잘라냅니다.**

`…&cropN=0,0,1,0.8&…`

## 참조 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [cropPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
