---
title: IccProfileGray
description: 회색 음영 기본 출력 색상 프로파일 출력 색상 공간이 icc=로 지정되지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 color= 등의 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 대해 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

회색 음영 기본 출력 색상 프로파일 출력 색상 공간이 icc=로 지정되지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 color= 등의 다양한 이미지 제공 명령으로 지정된 특정 회색 음영 색상 값에 대해 지정합니다.

## 속성 {#section-03f090ee2acf4537b83f78840d23ecab}

텍스트 문자열입니다. 지정되는 경우 유효해야 합니다. `icc::Name` 이 이미지 카탈로그나 기본 카탈로그의 ICC 프로파일 맵이나 `attribute::RootPath`. 참조된 ICC 프로파일은 회색 음영 프로필이어야 합니다.

## 기본값 {#section-95ba3ab15edc4259b657c6ebf8783d61}

상속됨 `default::IccProfileGray` 정의되지 않았거나 비어 있는 경우.

## 참조 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::이름](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [특성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [특성::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
