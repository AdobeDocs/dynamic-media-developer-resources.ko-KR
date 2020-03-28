---
description: 이미지 데이터 파일 경로. 이 카탈로그에 대한 이미지 데이터가 포함된 파일을 지정합니다.
seo-description: 이미지 데이터 파일 경로. 이 카탈로그에 대한 이미지 데이터가 포함된 파일을 지정합니다.
seo-title: CatalogFile
solution: Experience Manager
title: CatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 3599c8d3-dc4b-434e-8b11-775ea6f155ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CatalogFile{#catalogfile}

이미지 데이터 파일 경로. 이 카탈로그에 대한 이미지 데이터가 포함된 파일을 지정합니다.

이미지 데이터 파일은 지정된 순서대로 로드됩니다. 동일한 `catalog::Id` 값이 두 개 이상의 레코드(동일 또는 다른 카탈로그 파일)에서 발생하는 경우 마지막 인스턴스가 우선합니다.

## 속성 {#section-6da55f145ecd4e31a5de52637a436983}

하나 이상의 텍스트 문자열 값을 쉼표로 구분하여 지정합니다. 선택 사항입니다. 각 값은 카탈로그 폴더에 상대적인 절대 파일 경로나 경로여야 합니다.

## 기본값 {#section-80f91cd7a6b2479ebb310319e9c74da7}

비어 있음 - 이 이미지 카탈로그에 이미지 데이터가 포함되지 않음을 나타냅니다.

## 참조 {#section-910b67c5041d44d99a105ad43ff63a37}

[카탈로그 데이터 필드](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
