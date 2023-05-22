---
description: 기본 응답 이미지. 이미지를 찾을 수 없을 때 사용할 이미지 또는 카탈로그 항목을 지정합니다.
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---

# defaultImage{#defaultimage}

기본 응답 이미지. 이미지를 찾을 수 없을 때 사용할 이미지 또는 카탈로그 항목을 지정합니다.

` defaultImage= *`개체`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 오브젝트 </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 개체입니다. </p> </td> 
 </tr> 
</table>

*`object`* 카탈로그 항목(템플릿 포함) 또는 단순 이미지 파일 경로일 수 있습니다. 누락된 이미지를 기본 이미지로 대체하는 데 유용합니다. 이 값은 해당 카탈로그의 값을 재정의합니다. `attribute::DefaultImage`. 빈 값( `defaultImage=`) 기본 이미지 처리를 비활성화합니다.

>[!NOTE]
>
>기본 이미지 메커니즘은 SVG 개체에 적용되지 않습니다. 요청에 지정된 SVG 개체를 찾을 수 없는 경우 오류가 반환됩니다.

If `attribute::DefaultImageMode=0`, *`object`* 다중 이미지 컴포지션의 이미지 하나만 누락된 경우에도 전체 원본 요청을 대체합니다. 원본 요청에서 유지되는 유일한 명령은 다음과 같습니다. `wid=`, `hei=`, `fmt=`, `qlt=`.

If `attribute::DefaultImageMode=1`는 누락된 레이어 이미지만 대체합니다. 누락된 레이어에 대한 속성이 적용되고 합성이 평소대로 처리 및 반환됩니다.

## 속성 {#section-d30923d8dc4042eba10989212dd70887}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. 다음과 같은 경우 무시됨 `req=` 다음이 아님 `img` 또는 `tmb`.

## 제한 사항 {#section-30df31bc8cac41cd917f1e45196779c2}

외부 이미지 원본은 기본 이미지 메커니즘에 포함되지 않습니다. 외부 이미지 원본이 유효하지 않으면 오류가 반환됩니다.

이미지 제공이 (으)로 다시 되돌림 `DefaultImageMode=0` 중첩된 이미지 렌더링 또는 FXG 렌더링 요청이 실패할 경우.

## 기본값 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## 참조 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute:: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
