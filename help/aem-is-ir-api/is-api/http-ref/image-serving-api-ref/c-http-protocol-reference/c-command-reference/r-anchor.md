---
title: 앵커
description: 이미지 앵커. 변형(crop=, scale=, rotate=, flip=)을 적용하기 전에 이미지, 단색 또는 텍스트 테두리 상자 사각형의 기준점을 정의합니다. rotate=의 회전 중심 역할도 합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 2%

---

# 앵커{#anchor}

이미지 앵커. 변형(crop=, scale=, rotate=, flip=)을 적용하기 전에 이미지, 단색 또는 텍스트 테두리 상자 사각형의 기준점을 정의합니다. rotate=의 회전 중심 역할도 합니다.

`anchor= *`명령`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 열</span> </span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 왼쪽 위 모서리에서 픽셀 오프셋(int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>소스 이미지의 중심에서 정규화된 오프셋(실수, 실수) </p></td> 
 </tr> 
</table>

기준점은 이미지로 변환되고 레이어 원점이 됩니다(`origin=`도 지정되지 않은 경우 `anchor=`은(는) `rotate=`의 회전 중심으로만 사용됩니다).

`anchorN=0,0`이(가) 원본 이미지의 가운데에 이미지 앵커를 배치합니다. `anchorN=-0.5,-0.5` 또는 `anchor=0,0`은(는) 왼쪽 위 모서리에 있고 `anchorN=0.5,0.5`은(는) 소스 이미지의 오른쪽 아래 모서리에 있습니다.

## 속성 {#section-f08942bc6aae46a8b5d341faaff80640}

Source 이미지 속성입니다. `layer=comp`인 경우 현재 레이어 또는 레이어 0에 적용됩니다.

## 기본값 {#section-35d369fab1254f1a9b91684a6e169ad1}

`anchor=`을(를) 지정하지 않으면 catalog::Anchor가 사용됩니다. `catalog::Anchor`이(가) 정의되지 않으면 이미지 사각형의 중심이 사용됩니다(`anchorN=0,0`을(를) 지정하는 것과 동일).

`textPs=`을(를) 포함하는 텍스트 레이어와 `clipPath=`을(를) 포함하는 레이어는 서로 다른 기본 앵커를 가질 수 있습니다.

## 예 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)에서 &quot;예제 C&quot;를 참조하십시오.

## 참조 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[카탈로그::앵커](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [원본=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [회전=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [클립 경로=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [텍스트 레이어](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
