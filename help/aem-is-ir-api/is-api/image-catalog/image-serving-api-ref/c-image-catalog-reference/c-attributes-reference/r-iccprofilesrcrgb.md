---
description: RGB 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 RGB 소스 이미지 및 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-description: RGB 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 RGB 소스 이미지 및 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 RGB 소스 이미지 및 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-3cd753196959462e9e674dab0b033d08}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 관련 파일 경로여야 합니다 `attribute::RootPath`. 참조된 ICC 프로필은 RGB 프로필이어야 합니다.

## 기본값 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

정의되지 않았거나 비어 있는 `default::IccProfileSrcRgb` 경우 상속됩니다. 올바른 프로필로 확인되지 `attribute::IccProfileSrcRgb` 않으면 대신 `attribute::IccProfileRgb` 사용됩니다.

## 참조 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[attribute::IccProfileRgb,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)[속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
