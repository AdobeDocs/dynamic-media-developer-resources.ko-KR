---
title: IccProfileSrcCmyk
description: CMYK 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 CMYK 원본 이미지와 색상= 등의 다양한 이미지 제공 명령으로 지정된 특정 CMYK 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 CMYK 원본 이미지와 색상= 등의 다양한 이미지 제공 명령으로 지정된 특정 CMYK 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

텍스트 문자열입니다. 지정되는 경우 유효해야 합니다. `icc::Name` 이 이미지 카탈로그나 기본 카탈로그의 ICC 프로파일 맵이나 `attribute::RootPath`. 참조된 ICC 프로파일은 CMYK 프로파일이어야 합니다.

## 기본값 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

상속됨 `default::IccProfileSrcCmyk` 정의되지 않았거나 비어 있는 경우. If `attribute::IccProfileSrcCmyk` 올바른 프로필로 확인되지 않습니다. `attribute::IccProfileCmyk` 이 대신 사용됩니다.

## 참조 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::이름](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [특성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [특성::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
