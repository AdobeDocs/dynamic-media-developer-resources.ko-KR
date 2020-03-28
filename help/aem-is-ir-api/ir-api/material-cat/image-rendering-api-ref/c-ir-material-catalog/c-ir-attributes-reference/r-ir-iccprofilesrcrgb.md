---
description: RGB 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 RGB 질감 이미지 및 비네팅에 사용할 ICC 색상 프로파일의 이름과 bgc= 및 color= 등의 다양한 이미지 렌더링 명령으로 지정된 RGB 색상 값에 대한 이름을 지정합니다.
seo-description: RGB 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 RGB 질감 이미지 및 비네팅에 사용할 ICC 색상 프로파일의 이름과 bgc= 및 color= 등의 다양한 이미지 렌더링 명령으로 지정된 RGB 색상 값에 대한 이름을 지정합니다.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 9657e296-0d2a-4b05-9be7-5a54d3277f90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 RGB 질감 이미지 및 비네팅에 사용할 ICC 색상 프로파일의 이름과 bgc= 및 color= 등의 다양한 이미지 렌더링 명령으로 지정된 RGB 색상 값에 대한 이름을 지정합니다.

## 속성 {#section-c22966bba03e43c08e9d3fb91bfdd465}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 관련 파일 경로여야 합니다 `attribute::RootPath`. 참조된 ICC 프로필은 RGB 프로필이어야 합니다.

## 기본값 {#section-0171cd6680284bfa9844b9cc3644ca61}

정의되지 않았거나 비어 있는 `default::IccProfileSrcRgb` 경우 상속됩니다. 올바른 프로필로 확인되지 `attribute::IccProfileSrcRgb` 않으면 대신 `attribute::IccProfileRgb` 사용됩니다.

## 참조 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)[attribute::IccProfileRgb,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)[속성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
