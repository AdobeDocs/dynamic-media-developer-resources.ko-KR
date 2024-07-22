---
description: 기본 응답 이미지입니다. 이미지 파일을 찾을 수 없고 요청에 defaultImage= 가 지정되지 않은 경우 사용할 이미지 또는 카탈로그 항목을 지정합니다.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# DefaultImage{#defaultimage}

기본 응답 이미지입니다. 이미지 파일을 찾을 수 없고 요청에 defaultImage= 가 지정되지 않은 경우 사용할 이미지 또는 카탈로그 항목을 지정합니다.

카탈로그 항목(템플릿 포함) 또는 상대(`attribute::RootPath`) 또는 절대 이미지 파일 경로일 수 있습니다. 누락된 이미지를 기본 이미지로 대체하는 데 유용합니다.

## 속성 {#section-b6d8193827c34e5f948792aba8b8daaf}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그에 있는 올바른 `catalog::Id` 값이거나, `attribute::RootPath`에 대한 상대 경로이거나, 이미지 서버에서 액세스할 수 있는 이미지 파일의 절대 경로여야 합니다.

## 제한 사항 {#section-5d8ea872f0b0415fbd3a83410bbcf512}

외부 이미지 원본은 기본 이미지 메커니즘에 포함되지 않습니다. 외부 이미지 원본이 유효하지 않으면 오류가 반환됩니다.

## 기본값 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

정의되지 않은 경우 `default::DefaultImage`에서 상속됩니다. `default::DefaultImage`이(가) 정의되어 있더라도 비어 있으면 기본 이미지 동작이 비활성화됩니다.

## 참조 {#section-dc0fb4e72294442882b33a479fbc2b82}

[특성::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [특성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [카탈로그::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [특성::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [특성::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
