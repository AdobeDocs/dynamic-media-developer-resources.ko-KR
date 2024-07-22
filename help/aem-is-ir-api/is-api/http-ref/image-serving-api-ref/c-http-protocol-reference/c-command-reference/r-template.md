---
title: 템플릿
description: 템플릿 합성 중. 주 카탈로그가 아닌 카탈로그에 있는 합성 템플릿을 지정할 수 있도록 허용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 4%

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

*`template`*&#x200B;은(는) `catalog::Modifier`에 포함된 템플릿 본문이 있는 이미지 카탈로그 항목이어야 합니다.

`template=`이(가) 있으면 요청 경로에 지정된 개체가 레이어 0의 소스로 적용되지 않습니다. 그러나 미리 정의된 경로 변수 `$object$`을(를) `src=` 값으로 사용하여 템플릿의 어디에서나 `src=` 또는 `mask=`(으)로 참조할 수 있습니다. 요청 경로에 지정된 개체의 `catalog::Modifier`은(는) 템플릿 내에서 `$object$`의 대체로만 적용되지만 `catalog::PostModifier`은(는) 항상 적용됩니다.

레이어 0은 템플릿 본문에 정의되며 이미지, 단색, 텍스트 또는 중첩 또는 임베드된 요청 레이어가 될 수 있습니다.

*`object`*&#x200B;을(를) `template=`과(와) 함께 사용하면 *`object`*&#x200B;의 `catalog:PostModifier`이(가) 무시됩니다.

## 기본값 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

없음.

## 속성 {#section-daf3afb1d09c45a6a394468d0874c439}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다.

## 예 {#section-9a4f260ed43342b186b0fe855f34bca6}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)의 예제를 참조하십시오.

## 참조 {#section-067587444f774469931ecafd5a39834c}

[개체](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [미리 정의된 경로 변수](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
