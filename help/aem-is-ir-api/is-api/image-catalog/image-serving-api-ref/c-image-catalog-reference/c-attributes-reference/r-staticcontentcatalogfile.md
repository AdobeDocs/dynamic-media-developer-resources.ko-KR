---
description: 정적 콘텐츠 카탈로그 데이터 파일 경로. 이 카탈로그의 정적 콘텐츠 데이터를 포함하는 파일을 지정합니다.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

정적 콘텐츠 카탈로그 데이터 파일 경로. 이 카탈로그의 정적 콘텐츠 데이터를 포함하는 파일을 지정합니다.

정적 콘텐츠 카탈로그 데이터 파일은 지정된 순서대로 로드됩니다. 동일한 경우 `static::Id` 값이 두 개 이상의 레코드(동일한 카탈로그 파일 또는 다른 카탈로그 파일)에서 발생하고 마지막 인스턴스가 우세합니다.

## 속성 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

쉼표로 구분된 하나 이상의 텍스트 문자열 값. 선택적. 각 값은 카탈로그 폴더에 상대적인 절대 파일 경로 또는 경로여야 합니다.

## 기본값 {#section-702edfbc00c54fc29e412a3ff99fef2b}

비어 있음 - 이 이미지 카탈로그에 정적 콘텐츠 데이터가 포함되지 않음을 나타냅니다.

## 참조 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[카탈로그 데이터](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
