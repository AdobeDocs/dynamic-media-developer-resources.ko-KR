---
description: CMYK 기본 출력 색상 프로파일 icc=로 출력 색상 공간을 지정하지 않을 때 CMYK 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정하고 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 CMYK 색상 값에 대해 지정합니다.
seo-description: CMYK 기본 출력 색상 프로파일 icc=로 출력 색상 공간을 지정하지 않을 때 CMYK 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정하고 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 CMYK 색상 값에 대해 지정합니다.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: b22b6ed1-615f-4241-b4d4-c3aa70351458
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK 기본 출력 색상 프로파일 icc=로 출력 색상 공간을 지정하지 않을 때 CMYK 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정하고 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 CMYK 색상 값에 대해 지정합니다.

## 속성 {#section-d8b6102cc1c744d482f99808ccfcaa24}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 `attribute::RootPath`에 상대적인 파일 경로여야 합니다. 참조된 ICC 프로필은 CMYK 프로파일이어야 합니다.

## 기본값 {#section-62442df09a724950bfbdd0640b3e6678}

정의되지 않았거나 비어 있는 경우 `default::IccProfileCmyk`에서 상속됩니다.

## 참조 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [속성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [속성::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
