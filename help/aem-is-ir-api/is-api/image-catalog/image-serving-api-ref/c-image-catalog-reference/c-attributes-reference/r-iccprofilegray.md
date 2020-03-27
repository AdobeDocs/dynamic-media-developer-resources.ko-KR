---
description: 회색 음영 기본 출력 색상 프로파일 icc=로 출력 색상 공간을 지정하지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정하고 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 대해 지정합니다.
seo-description: 회색 음영 기본 출력 색상 프로파일 icc=로 출력 색상 공간을 지정하지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정하고 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 대해 지정합니다.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: a7d40114-f91f-4637-bb49-5b06b9ce846d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileGray{#iccprofilegray}

회색 음영 기본 출력 색상 프로파일 icc=로 출력 색상 공간을 지정하지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정하고 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 대해 지정합니다.

## 속성 {#section-03f090ee2acf4537b83f78840d23ecab}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 관련 파일 경로여야 합니다 `attribute::RootPath`. 참조된 ICC 프로필은 회색 음영 프로필이어야 합니다.

## 기본값 {#section-95ba3ab15edc4259b657c6ebf8783d61}

정의되지 않았거나 비어 있는 `default::IccProfileGray` 경우 상속됩니다.

## 참조 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[attribute::IccProfileSrcGray,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)[속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
