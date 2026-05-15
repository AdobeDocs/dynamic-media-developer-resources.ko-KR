---
title: IccProfileGray
description: 회색 음영 기본 색상 공간. icc=로 출력 색상 공간이 지정되지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
TQID: 'https://experienceleague.adobe.com/ZZOkc6f5V3-Luuwr5ku38nIy8snq4kh2lR4dqunXvFc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

회색 음영 기본 색상 공간. `icc=`(으)로 출력 색상 공간이 지정되지 않은 경우 회색 음영 응답 이미지에 사용할 ICC 색상 프로필의 이름을 지정합니다.

## 속성 {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

텍스트 문자열입니다. 지정하면 이 재질 카탈로그나 기본 카탈로그의 ICC 프로필 맵 또는 `attribute::RootPath`에 상대적인 파일 경로의 올바른 `icc::Name` 값이어야 합니다. 참조된 ICC 프로파일은 회색 음영 프로파일이어야 합니다.

## 기본값 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

정의되지 않았거나 비어 있는 경우 `default::IccProfileGray`에서 상속됩니다.

## 참조 {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [특성::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [특성::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [특성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
