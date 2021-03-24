---
description: RGB 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 RGB 질감 이미지 및 비네팅에 사용할 ICC 색상 프로파일의 이름과 bgc= 및 color=와 같은 다양한 이미지 렌더링 명령으로 지정된 RGB 색상 값에 대한 이름을 지정합니다.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 RGB 질감 이미지 및 비네팅에 사용할 ICC 색상 프로파일의 이름과 bgc= 및 color=와 같은 다양한 이미지 렌더링 명령으로 지정된 RGB 색상 값에 대한 이름을 지정합니다.

## 속성 {#section-c22966bba03e43c08e9d3fb91bfdd465}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 `attribute::RootPath`에 상대적인 파일 경로여야 합니다. 참조된 ICC 프로필은 RGB 프로필이어야 합니다.

## 기본값 {#section-0171cd6680284bfa9844b9cc3644ca61}

정의되지 않았거나 비어 있는 경우 `default::IccProfileSrcRgb`에서 상속됩니다. `attribute::IccProfileSrcRgb`이(가) 유효한 프로필로 확인되지 않으면 `attribute::IccProfileRgb`이(가) 대신 사용됩니다.

## 참조 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [속성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [속성::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [속성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
