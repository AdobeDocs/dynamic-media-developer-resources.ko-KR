---
description: 보기에 이미지 정렬을 참조하십시오. wid= 및 hei=로 정의된 보기 사각형 내에 비율 조정 후 합성 이미지를 정렬합니다(scl=도 지정되는 경우).
seo-description: 보기에 이미지 정렬을 참조하십시오. wid= 및 hei=로 정의된 보기 사각형 내에 비율 조정 후 합성 이미지를 정렬합니다(scl=도 지정되는 경우).
seo-title: 정렬
solution: Experience Manager
title: 정렬
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# align{#align}

보기에 이미지 정렬을 참조하십시오. wid= 및 hei=로 정의된 보기 사각형 내에 비율 조정 후 합성 이미지를 정렬합니다(scl=도 지정되는 경우).

` align= *``*, *`호리거`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 호리  </span> </span> </p> </td> 
  <td class="stentry"> <p>수평 정렬(실제, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 반전  </span> </span> </p> </td> 
  <td class="stentry"> <p>세로 정렬(실제, -1.0...1.0) </p> </td> 
 </tr> 
</table>

합성 이미지의 왼쪽 위 부분과 보기 왼쪽 위 부분을 정렬하려면 `align=-1,-1`을 지정하고, 이미지의 오른쪽 아래 부분을 보기 오른쪽 아래에 맞춰 정렬합니다. `align=1,1` 표준 이미지 및 축소판 요청의 경우 합성 이미지 데이터로 포함되지 않은 보기의 모든 영역이 `bgc=`으로 채워집니다.

## 속성 {#section-3fbec8206fc944eda4746d8be84f3b41}

속성을 봅니다. ( `align=`은(는) 워터마크가 적용된 합성 이미지와 워터마크 이미지 간의 정렬을 정의하는 데 사용됩니다.) 현재 레이어 설정에 관계없이 적용됩니다. `wid=` 및 `hei=` 중 하나만 지정되고 `fit=constrain` 또는 `fit=stretch`일 때 무시됩니다.

## 기본값 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`를 클릭하여 보기 사각형에 이미지를 배치합니다.

## 예 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

다음 요청은 `myImage`에 200x200 픽셀 보기 사각형을 적용합니다.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

`myImage`이 정사각형이면 전체 보기 사각형을 채웁니다. `myImage`에 세로 종횡비가 있는 경우 200픽셀로 크기가 조절되고 보기에서 가로로 가운데에 표시됩니다. `myImage`의 가로 종횡비가 있는 경우 가로 비율이 200픽셀로 조정되고 보기의 위쪽 가장자리에 정렬됩니다. 모든 경우 반환된 이미지의 크기는 정확히 200x200픽셀입니다.크기가 조정된 `myImage`에 포함되지 않은 모든 공간은 `attribute::BkgColor`(배경색을 동적으로 제어하려면 bgc= 지정)로 채워집니다.

## 참조 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) hei= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)fit= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)bgc= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)  [워터마크](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
