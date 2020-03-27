---
description: CMYK 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 CMYK 소스 이미지와 색상=와 같은 다양한 이미지 제공 명령으로 지정된 특정 CMYK 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-description: CMYK 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 CMYK 소스 이미지와 색상=와 같은 다양한 이미지 제공 명령으로 지정된 특정 CMYK 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 CMYK 소스 이미지와 색상=와 같은 다양한 이미지 제공 명령으로 지정된 특정 CMYK 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 관련 파일 경로여야 합니다 `attribute::RootPath`. 참조된 ICC 프로필은 CMYK 프로필이어야 합니다.

## 기본값 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

정의되지 않았거나 비어 있는 `default::IccProfileSrcCmyk` 경우 상속됩니다. 올바른 프로필로 확인되지 `attribute::IccProfileSrcCmyk` 않으면 대신 `attribute::IccProfileCmyk` 사용됩니다.

## 참조 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [속성::IccRenderIntent,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[속성::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
