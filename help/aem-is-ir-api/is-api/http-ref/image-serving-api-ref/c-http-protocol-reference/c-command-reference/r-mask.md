---
title: 마스크
description: 이미지 마스크입니다. 연결되지 않은 마스크로 사용할 별도의 마스크 이미지를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 1%

---

# 마스크{#mask}

이미지 마스크입니다. 연결되지 않은 마스크로 사용할 별도의 마스크 이미지를 지정합니다.

`mask= *`오브젝트`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 개체</span> </p></td> 
  <td class="stentry"> <p>이미지 또는 레이어 마스크로 사용할 이미지 개체입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>중첩 이미지 제공, 이미지 렌더링 또는 외부 요청. </p></td> 
 </tr> 
</table>

*`object`* 카탈로그 항목 또는 이미지/SVG 파일일 수 있습니다. 이미지 레이어 및 단색 레이어에 대해 지정할 수 있습니다.

If *`object`* 이미지 카탈로그 항목으로 확인됩니다. `catalog::MaskPath` 를 사용하거나, 다음과 같은 경우: `catalog::MaskPath` 가 정의되지 않은 경우 `catalog::Path` 를 사용합니다. If *`object`* 가 카탈로그 항목으로 확인되지 않으면 파일 경로로 해석됩니다.

모든 경우에 소스 이미지에 알파 채널이 있으면 이 채널이 사용됩니다. 그렇지 않으면 이미지를 레이어 마스크로 사용하기 전에 필요할 경우 회색 음영으로 변환됩니다.

마스크가 단색 레이어에 첨부된 경우 이미지 레이어의 이미지에 사용된 것과 동일한 규칙을 사용하여 마스크를 자르고 크기를 조정할 수 있습니다. `size=`, `scale=`, 또는 `res=` 를 사용하여 마스크 크기를 조정할 수 있습니다.

레이어 마스크는 *`nestedRequest`*. 중첩된 요청이나 포함된 요청은 중괄호로 묶입니다. 포함된 이미지 제공 요청 접두사로 사용 `is` 및 포함된 이미지 렌더링 요청 `ir`. 접두사가 지정되지 않은 경우 외부 서버 요청이 가정됩니다. 을(를) 참조하십시오 [중첩 및 포함 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) 을 참조하십시오.

## 속성 {#section-a093043dc249423b8ae322cefb0d545d}

이미지 또는 레이어 속성. 다음과 같은 경우 레이어 0에 적용됩니다. `layer=comp`. 효과 레이어에서 무시됨.

*`object`* 이 포함된 카탈로그 레코드로 확인해서는 안 됩니다. `src=` 또는 `mask=` 의 명령 `catalog::Modifier`.

다음 `is` 및 `ir` 접두사는 대/소문자를 구분하지 않습니다.

## 기본값 {#section-10cf793c665f49deb1b248faa3b618a9}

If `mask=` 가 명시적으로 지정되지 않고 레이어 이미지가 카탈로그 항목과 연결된 경우 `catalog::MaskPath` 를 사용합니다. 그렇지 않으면 레이어 이미지의 알파 채널이 사용됩니다(있는 경우). 알파 채널이 없으면 레이어에 마스크가 없고 레이어 사각형이 완전히 불투명하게 렌더링됩니다.

## 예 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

이미지의 여러 영역을 색상화하려면 여러 개의 개별 마스크를 사용합니다. 색상이 지정된 마스킹된 영역은 수정되지 않은 원본 이미지의 맨 위에 계층화됩니다.

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 참조 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [오브젝트](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [중첩 및 포함 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
