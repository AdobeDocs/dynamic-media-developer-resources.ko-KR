---
description: 이미지 앵커. 변형(crop=, scale=, rotate=, flip=)을 적용하기 전에 이미지, 단색 또는 텍스트 테두리 상자 사각형의 기준점을 정의합니다. rotate=의 회전 중심 역할도 합니다.
solution: Experience Manager
title: 앵커
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---

# 앵커{#anchor}

이미지 앵커. 변형(crop=, scale=, rotate=, flip=)을 적용하기 전에 이미지, 단색 또는 텍스트 테두리 상자 사각형의 기준점을 정의합니다. rotate=의 회전 중심 역할도 합니다.

`anchor= *`주역`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 주역</span> </span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리에서 픽셀 오프셋(int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 중심에서 정규화된 오프셋(실수, 실수) </p></td> 
 </tr> 
</table>

기준점은 이미지로 변환되고 레이어 원점이 됩니다(그렇지 않으면 `origin=` 이 경우에도 마찬가지로 지정되며, 이 경우 `anchor=` 의 회전 중심으로만 사용됩니다. `rotate=`).

`anchorN=0,0` 소스 이미지의 가운데에 이미지 앵커를 배치합니다. `anchorN=-0.5,-0.5` 또는 `anchor=0,0` 왼쪽 상단 모서리에 있습니다. `anchorN=0.5,0.5` 소스 이미지의 오른쪽 아래 모서리에 있습니다.

## 속성 {#section-f08942bc6aae46a8b5d341faaff80640}

소스 이미지 속성입니다. 다음과 같은 경우 현재 레이어 또는 레이어 0에 적용됩니다. `layer=comp`.

## 기본값 {#section-35d369fab1254f1a9b91684a6e169ad1}

If `anchor=` 이(가) 지정되지 않았습니다. catalog::Anchor가 사용됩니다. If `catalog::Anchor` 가 정의되지 않은 경우 이미지 사각형의 중심이 사용됩니다(지정과 동일) `anchorN=0,0`).

텍스트 레이어 관련 항목 `textPs=` 및 관련 레이어 `clipPath=` 는 다른 기본 앵커를 가질 수 있습니다.

## 예 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

에서 &quot;예 C&quot; 참조 [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[카탈로그::앵커](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [회전=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [텍스트 레이어](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
