---
description: CMYK 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 CMYK 재질 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-description: CMYK 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 CMYK 재질 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 95147b28-c87b-4337-a0eb-a962ca1e8786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK 기본 입력 색상 프로파일 색상 프로파일을 포함하지 않는 CMYK 재질 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-0cee77438d914c319ec876edb3490821}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 관련 파일 경로여야 합니다 `attribute::RootPath`. 참조된 ICC 프로필은 CMYK 프로필이어야 합니다.

## 기본값 {#section-11f6239e0dd14827abf4a95c1b30161c}

정의되지 않았거나 비어 있는 `default::IccProfileSrcCmyk` 경우 상속됩니다. 올바른 프로필로 확인되지 `attribute::IccProfileSrcCmyk` 않으면 대신 `attribute::IccProfileCmyk` 사용됩니다.

## 참조 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [속성::IccRenderIntent,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)[속성::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [속성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
