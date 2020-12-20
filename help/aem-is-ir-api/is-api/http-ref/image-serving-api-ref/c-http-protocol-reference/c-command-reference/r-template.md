---
description: 합성 템플릿. 기본 카탈로그 이외의 카탈로그에 있는 합성 템플릿을 지정할 수 있습니다.
seo-description: 합성 템플릿. 기본 카탈로그 이외의 카탈로그에 있는 합성 템플릿을 지정할 수 있습니다.
seo-title: 템플릿
solution: Experience Manager
title: 템플릿
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b37d60-1d0c-4d0b-a5a0-98d8bf9e9064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 6%

---


# 템플릿{#template}

합성 템플릿. 기본 카탈로그 이외의 카탈로그에 있는 합성 템플릿을 지정할 수 있습니다.

`template= *`템플릿`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 개체</span> </p> </td> 
  <td class="stentry"> <p>템플릿. </p></td> 
 </tr> 
</table>

*`template`* 은 에 포함된 템플릿 본문이 있는 이미지 카탈로그 항목이어야 합니다 `catalog::Modifier`.

`template=`이(가) 있으면 요청 경로에 지정된 객체가 레이어 0의 소스로 적용되지 않지만, 미리 정의된 경로 변수 `$object$`을(를) `src=` 값으로 사용하여 템플릿의 모든 위치에서 `src=` 또는 `mask=`로 참조할 수 있습니다. `catalog::Modifier` 요청 경로에 지정된 개체 수는 항상 적용되는 동안 템플릿 내 `$object$` 의 대체 개체와의 연결에만  `catalog::PostModifier` 적용됩니다.

레이어 0은 템플릿 본문에 정의되며 이미지, 단색, 텍스트 또는 중첩 또는 포함된 요청 레이어일 수 있습니다.

`catalog:PostModifier` 의 *`object`* 는 와 함께 사용할  *`object`* 때 무시됩니다 `template=`.

## 기본값 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

없음.

## 속성 {#section-daf3afb1d09c45a6a394468d0874c439}

요청 속성을 참조하십시오. 현재 레이어 설정에 관계없이 적용됩니다.

## 예 {#section-9a4f260ed43342b186b0fe855f34bca6}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)의 예를 참조하십시오.

## 참조 {#section-067587444f774469931ecafd5a39834c}

[개체](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [사전 정의된 경로 변수](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
