---
title: IccProfileCmyk
description: CMYK 기본 색상 공간. icc=로 출력 색상 공간이 지정되지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK 기본 색상 공간. `icc=`(으)로 출력 색상 공간이 지정되지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정합니다.

## 속성 {#section-849678b272954bdcb236f49aa54f1609}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵 또는 `attribute::RootPath`에 상대적인 파일 경로의 올바른 `icc::Name` 값이어야 합니다. 참조된 ICC 프로파일은 CMYK 프로파일이어야 합니다.

## 기본값 {#section-55026b7454af4d868bcb47f7743c9c5b}

정의되지 않았거나 비어 있는 경우 `default::IccProfileCmyk`에서 상속됩니다.

## 참조 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [특성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [특성::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [특성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
