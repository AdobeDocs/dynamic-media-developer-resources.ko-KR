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

RGB 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 재질 이미지와 비네팅 RGB에 사용할 ICC 색상 프로파일의 이름을 지정합니다. 다양한 이미지 렌더링 명령으로 지정된 RGB 색상 값에도 사용됩니다. `bgc=` 및 `color=`.

## 속성 {#section-c22966bba03e43c08e9d3fb91bfdd465}

텍스트 문자열입니다. 을(를) 지정한 경우 은(는) 유효해야 합니다. `icc::Name` 이 이미지 카탈로그나 기본 카탈로그의 ICC 프로파일 맵 또는 파일 경로의 값 `attribute::RootPath`. 참조된 ICC 프로파일은 RGB 프로파일이어야 합니다.

## 기본값 {#section-0171cd6680284bfa9844b9cc3644ca61}

상속 위치 `default::IccProfileSrcRgb` 정의되지 않은 경우 또는 비어 있는 경우. If `attribute::IccProfileSrcRgb` 이(가) 유효한 프로필로 확인되지 않습니다. `attribute::IccProfileRgb` 가 대신 사용됩니다.

## 참조 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
