---
description: RGB 기본 출력 색상 프로파일입니다. icc=로 출력 색상 공간이 지정되지 않은 경우 RGB 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 color= 등의 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 대해 지정합니다.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB 기본 출력 색상 프로파일입니다. icc=로 출력 색상 공간이 지정되지 않은 경우 RGB 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 color= 등의 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 대해 지정합니다.

## 속성 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

텍스트 문자열입니다. 지정한 경우 이 이미지 카탈로그나 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 `attribute::RootPath`에 상대적인 파일 경로여야 합니다. 참조된 ICC 프로파일은 RGB 프로파일이어야 합니다.

## 기본값 {#section-dfe08dd7b851453ca816623a4179955b}

정의되지 않았거나 비어 있는 경우 `default::IccProfileRgb`에서 상속됩니다.

## 참조 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [속성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [속성::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
