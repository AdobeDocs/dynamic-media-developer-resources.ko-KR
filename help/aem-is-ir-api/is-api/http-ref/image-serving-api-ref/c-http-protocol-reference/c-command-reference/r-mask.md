---
description: 이미지 마스크. 연결되지 않은 마스크로 사용할 별도의 마스크 이미지를 지정합니다.
seo-description: 이미지 마스크. 연결되지 않은 마스크로 사용할 별도의 마스크 이미지를 지정합니다.
seo-title: 마스크
solution: Experience Manager
title: 마스크
topic: Scene7 Image Serving - Image Rendering API
uuid: 2dc14d20-f02a-4a77-9b73-0c01e10d448d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 1%

---


# mask{#mask}

이미지 마스크. 연결되지 않은 마스크로 사용할 별도의 마스크 이미지를 지정합니다.

`mask= *``*|{[is|ir]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 개체</span> </p></td> 
  <td class="stentry"> <p>이미지 또는 레이어 마스크로 사용할 이미지 객체입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>중첩된 이미지 제공, 이미지 렌더링 또는 외부 요청. </p></td> 
 </tr> 
</table>

*`object`* 카탈로그 항목 또는 이미지/SVG 파일일 수 있습니다. 이미지 레이어 및 단색 레이어에 대해 지정할 수 있습니다.

*`object`*&#x200B;이 이미지 카탈로그 항목을 확인하면 `catalog::MaskPath`이 사용되거나, `catalog::MaskPath`가 정의되지 않은 경우 `catalog::Path`이(가) 사용됩니다. *`object`*&#x200B;이(가) 카탈로그 항목으로 확인되지 않으면 파일 경로로 해석됩니다.

모든 경우에 소스 이미지에 알파 채널이 있으면 이 채널이 사용됩니다. 그렇지 않으면 필요한 경우 레이어 마스크로 사용하기 전에 이미지가 회색 음영으로 변환됩니다.

단색 레이어에 마스크를 첨부하면 이미지 레이어의 이미지에 사용되는 것과 동일한 규칙을 사용하여 잘리고 크기를 조절할 수 있습니다. `size=`, 또는 마스크를 크기 조절하는 데 사용할  `scale=`  `res=` 수 있습니다.

레이어 마스크는 *`nestedRequest`* 형식으로 지정할 수도 있습니다. 중첩 또는 포함된 요청은 중괄호로 묶입니다. `is`으로 포함된 이미지 제공 요청과 `ir`로 포함된 이미지 렌더링 요청에 접두사를 붙입니다. 접두어가 지정되지 않은 경우 외국 서버에 대한 요청은 가정합니다. 자세한 내용은 [중첩 요청 및 포함](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)을 참조하십시오.

## 속성 {#section-a093043dc249423b8ae322cefb0d545d}

이미지 또는 레이어 속성입니다. `layer=comp`인 경우 레이어 0에 적용됩니다. 효과 레이어에서 무시됩니다.

*`object`* 의 또는 명령을 포함하는 카탈로그 레코드로  `src=` 확인할  `mask=` 수 없습니다 `catalog::Modifier`.

`is` 및 `ir` 접두사는 대소문자를 구분하지 않습니다.

## 기본값 {#section-10cf793c665f49deb1b248faa3b618a9}

`mask=`이(가) 명시적으로 지정되지 않은 경우 레이어 이미지가 카탈로그 항목과 연결된 경우 `catalog::MaskPath`이 사용됩니다. 그렇지 않으면 레이어 이미지의 알파 채널이 사용됩니다(있는 경우). 알파 채널이 없는 경우 레이어에 마스크가 없고 레이어 사각형이 완전히 불투명하게 렌더링됩니다.

## 예 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

여러 개의 개별 마스크를 사용하여 이미지의 다양한 영역에 색상을 적용할 수 있습니다. 색상화되고 마스크된 영역은 수정되지 않은 원본 이미지의 맨 위에 레이어됩니다.

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 참조 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [개체](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ,  [요청 중첩 및 포함](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
