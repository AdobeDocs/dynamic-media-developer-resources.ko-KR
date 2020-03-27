---
description: 레이어 배경색. 현재 레이어의 배경색과 불투명도를 지정합니다.
seo-description: 레이어 배경색. 현재 레이어의 배경색과 불투명도를 지정합니다.
seo-title: bgColor
solution: Experience Manager
title: bgColor
topic: Scene7 Image Serving - Image Rendering API
uuid: bcbd368f-d200-4b1f-8e9f-bf4d88f14b72
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgColor{#bgcolor}

레이어 배경색. 현재 레이어의 배경색과 불투명도를 지정합니다.

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 색상</span></span> </p> </td> 
  <td class="stentry"> <p>회색, RGB 또는 CMYK 색상 값(알파 포함 또는 알파 제외) </p></td> 
 </tr> 
</table>

레이어의 테두리 사각형 안에 있는 투명 및 반불투명 영역은* `opac=`뒤에 지정된 색상*으로 `rotate=`채워지고 `extend=` 적용됩니다.

## 속성 {#section-19dfc13e997f4a33889a1df1e4ad50b9}

레이어 특성. 현재 레이어나 레이어 0에 적용되는 경우 `layer=comp`입니다. 효과 레이어에서 무시됩니다.

*`color`* 는 의 픽셀 유형에 해당하는 작업 색상 공간에 존재하는 것으로 *`color`*&#x200B;가정합니다. *`color`* 최종 레이어 이미지의 픽셀 유형이 다른 경우 정확하게 변환됩니다.

## 기본값 {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0(완전 투명).

## 예 {#section-6e14fcf1d31e432dbdb56b9320904453}

자세한 내용은 [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## 참조 {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423), [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[extend, extend=Rotate=Rotate, bgcGc=Comp, Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
