---
description: RGB 기본 출력 색상 프로파일. icc=로 출력 색상 공간을 지정하지 않을 때 RGB 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 bgc= 및 color=와 같은 다양한 이미지 렌더링 명령으로 지정된 특정 RGB 색상 값에 대해 지정합니다.
seo-description: RGB 기본 출력 색상 프로파일. icc=로 출력 색상 공간을 지정하지 않을 때 RGB 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 bgc= 및 color=와 같은 다양한 이미지 렌더링 명령으로 지정된 특정 RGB 색상 값에 대해 지정합니다.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
uuid: 0fe63607-c328-468a-aa55-0c4d16cf9f0f
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# IccProfileRgb{#iccprofilergb}

RGB 기본 출력 색상 프로파일. icc=로 출력 색상 공간을 지정하지 않을 때 RGB 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정하고 bgc= 및 color=와 같은 다양한 이미지 렌더링 명령으로 지정된 특정 RGB 색상 값에 대해 지정합니다.

## 속성 {#section-b4a1bd92e99047479a5036413525a6d9}

텍스트 문자열. 지정된 경우 이 자료 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 `attribute::RootPath`에 상대적인 파일 경로여야 합니다. 참조된 ICC 프로필은 RGB 프로필이어야 합니다.

## 기본값 {#section-5809772f8e96438ab7626d323c66a4ba}

정의되지 않았거나 비어 있는 경우 `default::IccProfileRgb`에서 상속됩니다.

## 참조 {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [속성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [속성::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [속성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
