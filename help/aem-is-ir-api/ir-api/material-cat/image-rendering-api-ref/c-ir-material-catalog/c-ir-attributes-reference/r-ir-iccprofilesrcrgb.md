---
title: IccProfileSrcRgb
description: RGB 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 재질 이미지와 비네팅 RGB에 사용할 ICC 색상 프로파일의 이름을 지정합니다. 또한 bgc= 및 color= 등 다양한 이미지 렌더링 명령으로 지정된 RGB 색상 값입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 재질 이미지와 비네팅 RGB에 사용할 ICC 색상 프로파일의 이름을 지정합니다. `bgc=` 및 `color=` 등 다양한 이미지 렌더링 명령으로 지정된 RGB 색상 값에도 사용됩니다.

## 속성 {#section-c22966bba03e43c08e9d3fb91bfdd465}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵 또는 `attribute::RootPath`에 상대적인 파일 경로의 올바른 `icc::Name` 값이어야 합니다. 참조된 ICC 프로파일은 RGB 프로파일이어야 합니다.

## 기본값 {#section-0171cd6680284bfa9844b9cc3644ca61}

정의되지 않았거나 비어 있는 경우 `default::IccProfileSrcRgb`에서 상속됩니다. `attribute::IccProfileSrcRgb`이(가) 올바른 프로필로 확인되지 않으면 대신 `attribute::IccProfileRgb`이(가) 사용됩니다.

## 참조 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [특성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [특성::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [특성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
