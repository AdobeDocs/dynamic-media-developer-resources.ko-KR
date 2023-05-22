---
title: Icc 프로파일Rgb
description: RGB 기본 출력 색상 프로파일. icc=로 출력 색상 공간이 지정되지 않은 경우 RGB 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다. 또한 bgc= 및 color= 와 같은 다양한 이미지 렌더링 명령으로 지정된 특정 RGB 색상 값에 해당합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# Icc 프로파일Rgb{#iccprofilergb}

RGB 기본 출력 색상 프로파일. 출력 색상 공간이 지정되지 않은 경우 RGB 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다. `icc=`. 또한 다양한 이미지 렌더링 명령으로 지정된 특정 RGB 색상 값에 대해 다음과 같은 작업을 수행합니다. `bgc=` 및 `color=`.

## 속성 {#section-b4a1bd92e99047479a5036413525a6d9}

텍스트 문자열입니다. 을(를) 지정한 경우 은(는) 유효해야 합니다. `icc::Name` 이 재질 카탈로그나 기본 카탈로그의 ICC 프로파일 맵 또는 파일 경로의 값 `attribute::RootPath`. 참조된 ICC 프로파일은 RGB 프로파일이어야 합니다.

## 기본값 {#section-5809772f8e96438ab7626d323c66a4ba}

상속 위치 `default::IccProfileRgb` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
