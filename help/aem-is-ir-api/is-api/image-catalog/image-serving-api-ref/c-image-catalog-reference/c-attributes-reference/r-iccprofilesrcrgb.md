---
description: RGB 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 RGB 소스 이미지 및 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 RGB 소스 이미지 및 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-3cd753196959462e9e674dab0b033d08}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵 또는 `attribute::RootPath`에 상대적인 파일 경로의 올바른 `icc::Name` 값이어야 합니다. 참조된 ICC 프로파일은 RGB 프로파일이어야 합니다.

## 기본값 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

정의되지 않았거나 비어 있는 경우 `default::IccProfileSrcRgb`에서 상속됩니다. `attribute::IccProfileSrcRgb`이(가) 올바른 프로필로 확인되지 않으면 대신 `attribute::IccProfileRgb`이(가) 사용됩니다.

## 참조 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [특성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [특성::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [특성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
