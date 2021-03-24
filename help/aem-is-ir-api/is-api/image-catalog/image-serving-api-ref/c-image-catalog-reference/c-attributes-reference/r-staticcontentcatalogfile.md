---
description: 정적 컨텐츠 카탈로그 데이터 파일 경로. 이 카탈로그에 대한 정적 컨텐츠 데이터가 포함된 파일을 지정합니다.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

정적 컨텐츠 카탈로그 데이터 파일 경로. 이 카탈로그에 대한 정적 컨텐츠 데이터가 포함된 파일을 지정합니다.

정적 컨텐츠 카탈로그 데이터 파일은 지정된 순서대로 로드됩니다. 동일한 `static::Id` 값이 두 개 이상의 레코드(동일한 또는 다른 카탈로그 파일에서)에서 발생하는 경우 마지막 인스턴스가 우선합니다.

## 속성 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

하나 이상의 텍스트 문자열 값을 쉼표로 구분하여 지정합니다. 선택 사항입니다. 각 값은 카탈로그 폴더에 상대적인 절대 파일 경로 또는 경로여야 합니다.

## 기본값 {#section-702edfbc00c54fc29e412a3ff99fef2b}

비어 있음 - 이 이미지 카탈로그에 정적 컨텐츠 데이터가 포함되지 않음을 나타냅니다.

## 참조 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[카탈로그 데이터](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
