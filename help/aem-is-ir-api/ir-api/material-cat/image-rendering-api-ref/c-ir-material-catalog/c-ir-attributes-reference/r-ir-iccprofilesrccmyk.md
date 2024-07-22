---
title: IccProfileSrcCmyk
description: CMYK 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 CMYK 재질 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK 기본 입력 색상 프로파일. 색상 프로파일을 포함하지 않는 CMYK 재질 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.

## 속성 {#section-0cee77438d914c319ec876edb3490821}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵 또는 `attribute::RootPath`에 상대적인 파일 경로의 올바른 `icc::Name` 값이어야 합니다. 참조된 ICC 프로파일은 CMYK 프로파일이어야 합니다.

## 기본값 {#section-11f6239e0dd14827abf4a95c1b30161c}

정의되지 않았거나 비어 있는 경우 `default::IccProfileSrcCmyk`에서 상속됩니다. `attribute::IccProfileSrcCmyk`이(가) 올바른 프로필로 확인되지 않으면 대신 `attribute::IccProfileCmyk`이(가) 사용됩니다.

## 참조 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [특성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [특성::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [특성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
