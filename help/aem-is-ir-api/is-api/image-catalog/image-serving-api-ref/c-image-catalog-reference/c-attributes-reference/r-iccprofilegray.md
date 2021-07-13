---
description: 회색 음영 기본 출력 색상 프로파일 출력 색상 공간이 icc=로 지정되지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 color= 등의 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 대해 지정합니다.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

회색 음영 기본 출력 색상 프로파일 출력 색상 공간이 icc=로 지정되지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 color= 등의 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 대해 지정합니다.

## 속성 {#section-03f090ee2acf4537b83f78840d23ecab}

텍스트 문자열입니다. 지정한 경우 이 이미지 카탈로그나 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 `attribute::RootPath`에 상대적인 파일 경로여야 합니다. 참조된 ICC 프로파일은 회색 음영 프로필이어야 합니다.

## 기본값 {#section-95ba3ab15edc4259b657c6ebf8783d61}

정의되지 않았거나 비어 있는 경우 `default::IccProfileGray`에서 상속됩니다.

## 참조 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [속성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [속성::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9),  [속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
