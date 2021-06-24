---
description: 기본 회신 이미지. 이미지를 찾을 수 없을 때 사용할 이미지 또는 카탈로그 항목을 지정합니다.
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# defaultImage{#defaultimage}

기본 회신 이미지. 이미지를 찾을 수 없을 때 사용할 이미지 또는 카탈로그 항목을 지정합니다.

` defaultImage= *`개체`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 개체  </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 개체. </p> </td> 
 </tr> 
</table>

*`object`* 카탈로그 항목(템플릿 포함) 또는 단순 이미지 파일 경로일 수 있습니다. 누락된 이미지를 기본 이미지로 대체하는 데 유용합니다. 이 값은 해당 카탈로그 `attribute::DefaultImage` 값을 재정의합니다. 빈 값( `defaultImage=`)은 기본 이미지 처리를 비활성화합니다.

>[!NOTE]
>
>기본 이미지 메커니즘은 SVG 개체에 적용되지 않습니다. 요청에 지정된 SVG 개체를 찾을 수 없으면 오류가 반환됩니다.

`attribute::DefaultImageMode=0`이면 다중 이미지 컴포지션에 있는 이미지가 하나만 없는 경우에도 *`object`*&#x200B;이 전체 원본 요청을 대체합니다. 원래 요청에서 유지된 유일한 명령은 다음과 같습니다.`wid=`, `hei=`, `fmt=`, `qlt=`.

`attribute::DefaultImageMode=1`이면 누락된 레이어 이미지만 개체가 대체합니다.누락된 레이어에 대한 속성이 적용되어 컴포지션이 처리되어 평소대로 반환됩니다.

## 속성 {#section-d30923d8dc4042eba10989212dd70887}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. `req=`이 `img` 또는 `tmb`가 아닌 경우 무시됩니다.

## 제한 사항 {#section-30df31bc8cac41cd917f1e45196779c2}

외부 이미지 소스는 기본 이미지 메커니즘으로 적용되지 않습니다.외부 이미지 소스가 유효하지 않은 경우 오류가 반환됩니다.

중첩 이미지 렌더링 또는 FXG 렌더링 요청이 실패할 경우 이미지 제공은 다시 `DefaultImageMode=0` 로 되돌아갑니다.

## 기본값 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## 참조 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [attribute:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
