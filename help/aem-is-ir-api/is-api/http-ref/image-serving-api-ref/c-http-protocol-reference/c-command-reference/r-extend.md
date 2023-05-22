---
description: 레이어를 확장합니다. 레이어에 여백을 추가하거나 레이어 사각형을 자릅니다.
solution: Experience Manager
title: 확장
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# 확장{#extend}

레이어를 확장합니다. 레이어에 여백을 추가하거나 레이어 사각형을 자릅니다.

`extend= *`left`*, *`top`*, *`오른쪽`*, *`bottom`*`

`extendN= *`왼쪽 N`*, *`topN`*, *`오른쪽`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 왼쪽, 위쪽, 아래쪽, 오른쪽</span></span> </p></td> 
  <td class="stentry"> <p>레이어 rect의 왼쪽, 위쪽, 오른쪽 및 아래쪽 가장자리(int, int, int, int)에 추가하거나 제거할 픽셀 수. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>레이어 rect의 왼쪽, 위쪽, 오른쪽 및 아래쪽 가장자리에 추가하거나 제거할 공간의 양으로서 원래 레이어 rect(실수, 실수, 실수, 실수)의 크기에 대해 표준화된 양으로 표시됩니다. </p></td> 
 </tr> 
</table>

`extend=` 레이어에 적용됨 *이후* 이미지가 잘립니다( `crop=`) 및 다음을 포함한 모든 레이어 변환 `rotate=`이 적용되었습니다.

확장된 영역은 다음으로 채워짐 `bgColor=`또는 지정하지 않으면 투명하게 유지됩니다.

인수 값 `extendN=` 다음을 포함한 레이어 변환 후 레이어 rect의 크기에 따라 표준화됩니다. `rotate=` 이(가) 적용되었습니다.

## 속성 {#section-8fc94de871f841f3bf5e1df135972ca9}

레이어 속성입니다. 다음과 같은 경우 레이어 0에 적용됩니다. `layer=comp`. 효과 레이어에서 무시됨.

## 기본값 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`레이어 사각형을 변경하지 않는 경우입니다.

## 예제 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**이미지를 자른 다음 5픽셀 너비의 빨간색 테두리를 추가합니다.**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**이미지를 200픽셀 너비로 조정하고 제목 텍스트를 이미지 위의 30픽셀 여백에 추가합니다.**

합성 이미지의 높이는 이미지의 종횡비에 따라 달라집니다.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 참조 {#section-2d9572be32ca4602b60920b3810f3638}

[자르기=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
