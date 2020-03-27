---
description: 레이어 확장 레이어에 여백을 추가하거나 레이어 사각형을 자릅니다.
seo-description: 레이어 확장 레이어에 여백을 추가하거나 레이어 사각형을 자릅니다.
seo-title: extend
solution: Experience Manager
title: extend
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# extend{#extend}

레이어 확장 레이어에 여백을 추가하거나 레이어 사각형을 자릅니다.

`extend= *``*, *``*, *``*, *`왼쪽 맨 아래`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 왼쪽,위쪽,아래쪽,오른쪽 <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>레이어 rect의 왼쪽, 위쪽, 오른쪽 및 아래쪽 가장자리(int, int, int)에 추가할 픽셀 수입니다(또는 값이 음수인 경우 제거할 픽셀 수). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 왼쪽N,topN,아래쪽N,오른쪽</span></span> </p></td> 
  <td class="stentry"> <p>레이어 사각형의 왼쪽, 위쪽, 오른쪽 및 아래쪽 가장자리에 추가할 공간(또는 값이 음수이면 제거할 공간)(원본 레이어 사각형의 크기(실제, 실제, 실제)에 상대적인 정규화된 금액으로 표시됨) </p></td> 
 </tr> 
</table>

`extend=` 이미지가 잘린 *후* 레이어에 적용되고( `crop=`) 모든 레이어 변형(예: `rotate=`적용)이 적용됩니다.

확장 영역이 `bgColor=`채워지거나 지정되지 않은 경우 투명하게 유지됩니다.

에 대한 인수 값은 적용된 것을 포함하여 레이어 변형 후 레이어 사각형 크기를 기준으로 표준화됩니다. `extendN=` `rotate=`

## 속성 {#section-8fc94de871f841f3bf5e1df135972ca9}

레이어 특성. 해당되는 경우 레이어 0에 `layer=comp`적용됩니다. 효과 레이어에서 무시됩니다.

## 기본값 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`를 클릭하여 레이어 사각형을 변경하지 않습니다.

## 예제 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**이미지를 자른 다음 5픽셀 너비의 빨간색 테두리를 추가합니다.**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**이미지의 크기를 200픽셀 너비로 조정하고 제목 텍스트를 이미지 위의 30픽셀 여백에 추가합니다.**

합성 이미지의 높이는 이미지의 종횡비에 따라 다릅니다.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 참조 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) color= [,](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)size= [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)[covering, clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
