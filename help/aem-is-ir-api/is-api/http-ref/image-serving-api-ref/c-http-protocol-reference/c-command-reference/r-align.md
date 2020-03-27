---
description: 보기를 사용하여 이미지 정렬. wid= 및 hei=로 정의된 보기 사각형 내에 비율 조정 후(scl=도 지정된 경우) 합성 이미지를 정렬합니다.
seo-description: 보기를 사용하여 이미지 정렬. wid= 및 hei=로 정의된 보기 사각형 내에 비율 조정 후(scl=도 지정된 경우) 합성 이미지를 정렬합니다.
seo-title: 정렬
solution: Experience Manager
title: 정렬
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

보기를 사용하여 이미지 정렬. wid= 및 hei=로 정의된 보기 사각형 내에 비율 조정 후(scl=도 지정된 경우) 합성 이미지를 정렬합니다.

` align= *``*, *`호리자리`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 호리스 </span></span> </p> </td> 
  <td class="stentry"> <p>수평 정렬(실제, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 반전 </span></span> </p> </td> 
  <td class="stentry"> <p>세로 정렬(실제, -1.0...1.0) </p> </td> 
 </tr> 
</table>

합성 이미지의 왼쪽 `align=-1,-1` 위쪽을 보기의 왼쪽 위에 정렬하도록 지정하고, 이미지의 오른쪽 아래 부분을 보기의 오른쪽 아래에 정렬하도록 `align=1,1` 지정합니다. 표준 이미지 및 축소판 요청의 경우 복합 이미지 데이터로 포함되지 않은 보기의 모든 영역이 채워집니다 `bgc=`.

## 속성 {#section-3fbec8206fc944eda4746d8be84f3b41}

속성을 봅니다. ( `align=` 는 워터마크 이미지와 워터마크가 적용되는 합성 이미지 간의 정렬을 정의하는 데도 사용됩니다.) 현재 레이어 설정에 관계없이 적용됩니다. 하나만 `wid=` 지정되고 `hei=` 지정된 경우 `fit=constrain` 또는 `fit=stretch`지정된 경우 무시됩니다.

## 기본값 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`를 클릭합니다.

## 예 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

다음 요청은 200x200 픽셀 보기 사각형에 `myImage` 해당합니다.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

정확히 정사각형이면 전체 보기 사각형을 채웁니다. `myImage` 세로 종횡비가 `myImage` 있는 경우 200픽셀로 크기가 조절되고 보기에서 가로로 가운데에 정렬됩니다. 가로 종횡비가 `myImage` 있는 경우 200픽셀로 크기가 조절되고 보기의 위쪽 가장자리에 정렬됩니다. 모든 경우 반환된 이미지의 크기는 정확히 200x200픽셀입니다.크기를 조절하지 않은 모든 공간은 `myImage` 채워집니다(배경색을 동적으로 제어하려면 bgc=를 `attribute::BkgColor` 지정합니다).

## 참조 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) hei= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)fit= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)bgc= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[워터마크](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
