---
description: 회색 음영 기본 색상 공간. icc=로 출력 색상 공간을 지정하지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정합니다.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# IccProfileGray{#iccprofilegray}

회색 음영 기본 색상 공간. icc=로 출력 색상 공간을 지정하지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정합니다.

## 속성 {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

텍스트 문자열. 지정된 경우 이 자료 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵에서 유효한 `icc::Name` 값이거나 `attribute::RootPath`에 상대적인 파일 경로여야 합니다. 참조된 ICC 프로필은 회색 음영 프로필이어야 합니다.

## 기본값 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

정의되지 않았거나 비어 있는 경우 `default::IccProfileGray`에서 상속됩니다.

## 참조 {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [속성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [속성::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2),  [속성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
