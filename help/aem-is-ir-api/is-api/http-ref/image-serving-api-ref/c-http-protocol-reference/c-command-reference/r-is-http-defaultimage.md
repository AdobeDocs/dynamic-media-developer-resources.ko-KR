---
description: 기본 응답 이미지를 참조하십시오. 이미지를 찾을 수 없을 때 사용할 이미지 또는 카탈로그 항목을 지정합니다.
seo-description: 기본 응답 이미지를 참조하십시오. 이미지를 찾을 수 없을 때 사용할 이미지 또는 카탈로그 항목을 지정합니다.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7478325c-9ac5-4b85-a4c5-5c495f924eb5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---


# defaultImage{#defaultimage}

기본 응답 이미지를 참조하십시오. 이미지를 찾을 수 없을 때 사용할 이미지 또는 카탈로그 항목을 지정합니다.

` defaultImage= *`개체`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 개체  </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 개체. </p> </td> 
 </tr> 
</table>

*`object`* 카탈로그 항목(템플릿 포함) 또는 단순 이미지 파일 경로일 수 있습니다. 누락된 이미지를 기본 이미지로 대체하는 데 유용합니다. 이 값은 해당 카탈로그 `attribute::DefaultImage`의 값을 무시합니다. 빈 값( `defaultImage=`)은 기본 이미지 처리를 비활성화합니다.

>[!NOTE]
>
>기본 이미지 메커니즘은 SVG 개체에 적용되지 않습니다. 요청에 지정된 SVG 개체를 찾을 수 없는 경우 오류가 반환됩니다.

`attribute::DefaultImageMode=0`의 경우 다중 이미지 컴포지션에 하나의 이미지만 누락되더라도 *`object`*&#x200B;은 전체 원본 요청을 대체합니다. 원래 요청에서 유지된 유일한 명령은 다음과 같습니다.`wid=`, `hei=`, `fmt=`, `qlt=`.

`attribute::DefaultImageMode=1`인 경우 개체는 누락된 레이어 이미지만 대체합니다.누락된 레이어에 대한 속성이 적용되고 합성이 평소대로 처리되고 반환됩니다.

## 속성 {#section-d30923d8dc4042eba10989212dd70887}

요청 속성을 참조하십시오. 현재 레이어 설정에 관계없이 적용됩니다. `req=`이(가) `img` 또는 `tmb` 이외의 경우 무시됩니다.

## 제한 사항 {#section-30df31bc8cac41cd917f1e45196779c2}

외부 이미지 소스는 기본 이미지 메커니즘에 포함되지 않습니다.외부 이미지 소스가 유효하지 않은 경우 오류가 반환됩니다.

중첩된 이미지 렌더링 또는 FXG 렌더링 요청이 실패하면 이미지 제공 시 다시 `DefaultImageMode=0`으로 돌아갑니다.

## 기본값 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## 참조 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [특성::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
