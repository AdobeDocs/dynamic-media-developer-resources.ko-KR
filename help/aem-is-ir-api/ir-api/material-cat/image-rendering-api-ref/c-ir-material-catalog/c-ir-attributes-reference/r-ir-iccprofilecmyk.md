---
description: CMYK 기본 색상 공간. icc=로 지정된 출력 색상 공간이 없을 때 회색 음영 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-description: CMYK 기본 색상 공간. icc=로 지정된 출력 색상 공간이 없을 때 회색 음영 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: d923d0fd-f00b-4fce-8ce9-8b177b4dba96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK 기본 색상 공간. icc=로 지정된 출력 색상 공간이 없을 때 회색 음영 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-849678b272954bdcb236f49aa54f1609}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 관련 파일 경로여야 합니다 `attribute::RootPath`. 참조된 ICC 프로필은 CMYK 프로필이어야 합니다.

## 기본값 {#section-55026b7454af4d868bcb47f7743c9c5b}

정의되지 않았거나 비어 있는 `default::IccProfileCmyk` 경우 상속됩니다.

## 참조 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [속성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [속성::IccProfileSrcCmyk,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2)[속성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
