---
description: 템플릿 합성 중. 주 카탈로그가 아닌 카탈로그에 있는 합성 템플릿을 지정할 수 있도록 허용합니다.
solution: Experience Manager
title: 템플릿
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 6%

---

# 템플릿{#template}

템플릿 합성 중. 주 카탈로그 이외의 카탈로그에 합성 템플릿을 지정할 수 있습니다.

`template= *`템플릿`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 개체</span> </p> </td> 
  <td class="stentry"> <p>템플릿. </p></td> 
 </tr> 
</table>

*`template`* 은(는) 템플릿 본문이 포함된 이미지 카탈로그 항목이어야 합니다. `catalog::Modifier`.

날짜 `template=` 이(가) 있으면 요청 경로에 지정된 개체가 레이어 0의 소스로 적용되지 않습니다. 그러나 로 참조할 수 있습니다. `src=` 또는 `mask=` 사전 정의된 경로 변수를 사용하여 템플릿의 모든 위치 `$object$` as a `src=` 값. `catalog::Modifier` 요청 경로에 지정된 개체의 는 `$object$` 템플릿 내에 있는 반면 `catalog::PostModifier` 는 항상 적용됩니다.

레이어 0은 템플릿 본문에 정의되며 이미지, 단색, 텍스트 또는 중첩 또는 임베드된 요청 레이어가 될 수 있습니다.

`catalog:PostModifier` / *`object`* 은(는) 다음의 경우 무시됩니다. *`object`* 과 함께 사용됨 `template=`.

## 기본값 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

없음.

## 속성 {#section-daf3afb1d09c45a6a394468d0874c439}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다.

## 예 {#section-9a4f260ed43342b186b0fe855f34bca6}

의 예를 참조하십시오. [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-067587444f774469931ecafd5a39834c}

[오브젝트](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [사전 정의된 경로 변수](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
