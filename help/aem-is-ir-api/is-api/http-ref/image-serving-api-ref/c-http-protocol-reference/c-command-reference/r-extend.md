---
description: 레이어 확장 레이어에 여백을 추가하거나 레이어 사각형을 자릅니다.
seo-description: 레이어 확장 레이어에 여백을 추가하거나 레이어 사각형을 자릅니다.
seo-title: extend
solution: Experience Manager
title: extend
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# extend{#extend}

레이어 확장 레이어에 여백을 추가하거나 레이어 사각형을 자릅니다.

`extend= *``*, *``*, *``*, *`왼쪽 맨 아래`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 왼쪽,위쪽,아래쪽,오른쪽</span></span> </p></td> 
  <td class="stentry"> <p>레이어 rect의 왼쪽, 위쪽, 오른쪽 및 아래쪽 가장자리(int, int, int)에 추가할 픽셀 수입니다(값이 음수인 경우 이 값을 제거합니다). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>원래 레이어 사각형 크기(실제, 실제, 실제)에 상대적으로 정규화된 금액으로 표현되는 레이어 rect의 왼쪽, 위, 오른쪽 및 아래쪽 가장자리에 추가할 공간(값이 음수인 경우 이 값에서 제거)입니다. </p></td> 
 </tr> 
</table>

`extend=` 이미지가 잘린  ** 후( `crop=`) 레이어에 적용되고 이미지를 비롯한 모든 레이어 변형 `rotate=`이 적용되었습니다.

확장 영역은 `bgColor=`으로 채워지거나, 지정하지 않은 경우 투명하게 유지됩니다.

`extendN=`의 인수 값은 `rotate=`이 적용된 레이어 변형 후 레이어 사각형 크기를 기준으로 표준화됩니다.

## 속성 {#section-8fc94de871f841f3bf5e1df135972ca9}

레이어 속성입니다. `layer=comp`인 경우 레이어 0에 적용됩니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`를 클릭하여 레이어 사각형을 변경하지 않습니다.

## 예제 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**이미지를 자른 다음 5픽셀의 빨강 테두리를 추가합니다.**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**이미지의 크기를 200픽셀 폭으로 조정하고 제목 텍스트를 이미지 위의 30픽셀 여백에 추가합니다.**

합성 이미지의 높이는 이미지의 종횡비에 따라 달라집니다.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 참조 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), origin= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
