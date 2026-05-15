---
description: RGB 기본 출력 색상 프로파일. icc=로 출력 색상 공간이 지정되지 않은 경우 RGB 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정하고 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 사용할 수 있습니다.
solution: Experience Manager
title: Icc 프로파일Rgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
TQID: 'https://experienceleague.adobe.com/U9-XwSInZJDmRhDLPVzLqJds28LVZm3LkJE0iD7KEps'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

---

# Icc 프로파일Rgb{#iccprofilergb}

RGB 기본 출력 색상 프로파일. icc=로 출력 색상 공간이 지정되지 않은 경우 RGB 응답 이미지에 사용할 ICC 색상 프로파일의 이름을 지정하고 color=와 같은 다양한 이미지 제공 명령으로 지정된 특정 RGB 색상 값에 사용할 수 있습니다.

## 속성 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그 또는 기본 카탈로그의 ICC 프로필 맵 또는 `attribute::RootPath`에 상대적인 파일 경로의 올바른 `icc::Name` 값이어야 합니다. 참조된 ICC 프로필은 RGB 프로필이어야 합니다.

## 기본값 {#section-dfe08dd7b851453ca816623a4179955b}

정의되지 않았거나 비어 있는 경우 `default::IccProfileRgb`에서 상속됩니다.

## 참조 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [특성::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [특성::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2), [특성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
