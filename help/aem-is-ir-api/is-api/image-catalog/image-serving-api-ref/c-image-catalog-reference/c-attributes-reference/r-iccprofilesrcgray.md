---
description: 회색 음영 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 회색 음영 소스 이미지 및 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcGray{#iccprofilesrcgray}

회색 음영 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 회색 음영 소스 이미지 및 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-8cbb316df6eb463aaca7b308d3568086}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵 또는 `attribute::RootPath`에 상대적인 파일 경로의 올바른 `icc::Name` 값이어야 합니다. 참조된 ICC 프로파일은 회색 음영 프로파일이어야 합니다.

## 기본값 {#section-bcc7250715884412bd0780f60d1cce7b}

정의되지 않았거나 비어 있는 경우 `default::IccProfileSrcGray`에서 상속됩니다. `attribute::IccProfileSrcGray`이(가) 올바른 프로필로 확인되지 않으면 대신 `attribute::IccProfileGray`이(가) 사용됩니다.

## 참조 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [특성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [특성::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35), [특성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
