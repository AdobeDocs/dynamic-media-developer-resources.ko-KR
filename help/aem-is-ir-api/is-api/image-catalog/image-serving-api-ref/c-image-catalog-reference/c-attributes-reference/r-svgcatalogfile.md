---
description: SVG 데이터 파일 경로 이 카탈로그에 대한 SVG 데이터가 포함된 파일을 지정합니다.
seo-description: SVG 데이터 파일 경로 이 카탈로그에 대한 SVG 데이터가 포함된 파일을 지정합니다.
seo-title: SvgCatalogFile
solution: Experience Manager
title: SvgCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SvgCatalogFile{#svgcatalogfile}

SVG 데이터 파일 경로 이 카탈로그에 대한 SVG 데이터가 포함된 파일을 지정합니다.

SVG 데이터 파일은 지정된 정확한 순서로 모든 이미지 데이터 파일 뒤에 로드됩니다. 동일한 `catalog::Id` 값이 두 개 이상의 레코드(동일하거나 다른 이미지 또는 SVG 카탈로그 파일)에서 발생하는 경우 마지막 인스턴스가 우선합니다.

## 속성 {#section-fc2d549f76474792837b2b92ec2087ea}

하나 이상의 텍스트 문자열 값을 쉼표로 구분하여 지정합니다. 선택 사항입니다. 각 값은 카탈로그 폴더에 상대적인 절대 파일 경로나 경로여야 합니다.

## 기본값 {#section-a4e58951f3c249599665b823566433c9}

비어 있음 - 이 이미지 카탈로그에 SVG 데이터가 포함되지 않음을 나타냅니다.

## 참조 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[카탈로그 데이터](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
