---
description: 회색 음영 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 회색 음영 재질 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-description: 회색 음영 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 회색 음영 재질 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

회색 음영 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 회색 음영 재질 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-97923d8561b845309442d57d017d91a4}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 관련 파일 경로여야 합니다 `attribute::RootPath`. 참조된 ICC 프로필은 회색 음영 프로필이어야 합니다.

## 기본값 {#section-02c52805ee13483dba7878aeab51f889}

정의되지 않았거나 비어 있는 `default::IccProfileSrcGray` 경우 상속됩니다. 올바른 프로필로 확인되지 `attribute::IccProfileSrcGray` 않으면 대신 `attribute::IccProfileGray` 사용됩니다.

## 참조 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)[attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [속성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
