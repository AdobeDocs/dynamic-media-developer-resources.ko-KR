---
description: 이미지 앵커. 변형(crop=, scale=, rotate=, flip=)을 적용하기 전에 이미지, 단색 또는 텍스트 테두리 상자 사각형의 기준점을 정의합니다. 또한 rotate=의 회전 중심 역할을 합니다.
seo-description: 이미지 앵커. 변형(crop=, scale=, rotate=, flip=)을 적용하기 전에 이미지, 단색 또는 텍스트 테두리 상자 사각형의 기준점을 정의합니다. 또한 rotate=의 회전 중심 역할을 합니다.
seo-title: 앵커
solution: Experience Manager
title: 앵커
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 앵커{#anchor}

이미지 앵커. 변형(crop=, scale=, rotate=, flip=)을 적용하기 전에 이미지, 단색 또는 텍스트 테두리 상자 사각형의 기준점을 정의합니다. 또한 rotate=의 회전 중심 역할을 합니다.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 코드</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모퉁이에서 픽셀 오프셋(int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 중심에서 정규화된 오프셋(실제, 실제) </p></td> 
 </tr> 
</table>

고정점은 이미지와 함께 변형되어 레이어 원점이 됩니다( `origin=` 이 경우에도 지정되어 있지 않으면 레이어 원점, 이 경우 회전 중심으로만 `anchor=` 사용됩니다 `rotate=`).

`anchorN=0,0` 소스 이미지의 중앙에 이미지 앵커를 배치합니다. `anchorN=-0.5,-0.5` 또는 `anchor=0,0` 왼쪽 위 모퉁이에 있고 소스 이미지의 오른쪽 아래에 `anchorN=0.5,0.5` 있습니다.

## 속성 {#section-f08942bc6aae46a8b5d341faaff80640}

소스 이미지 속성입니다. 현재 레이어나 레이어 0에 적용되는 경우 `layer=comp`입니다.

## 기본값 {#section-35d369fab1254f1a9b91684a6e169ad1}

지정하지 `anchor=` 않으면 catalog::Anchor가 사용됩니다. 을 `catalog::Anchor` 정의하지 않으면 이미지 사각형의 중심이 사용됩니다(지정하는 것과 `anchorN=0,0`같음).

관련된 `textPs=` 및 레이어와 관련된 텍스트 레이어에는 다른 기본 앵커가 있을 `clipPath=` 수 있습니다.

## 예 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

템플릿의 &quot;예제 C&quot;를 [참조하십시오](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[, AnchorText Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
