---
description: 소스 데이터 루트 경로. 이 이미지 카탈로그의 소스 데이터에 대한 루트 폴더의 절대 또는 상대 경로입니다.
solution: Experience Manager
title: 루트 경로
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# 루트 경로{#rootpath}

소스 데이터 루트 경로. 이 이미지 카탈로그의 소스 데이터에 대한 루트 폴더의 절대 또는 상대 경로입니다.

`RootPath`은 텍스트 문자열 값입니다. 서버 루트 경로에 대한 자세한 내용은 [소스 데이터 관리](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)를 참조하십시오.

## 속성 {#section-b41d7e0ea63143eb8034569706cad0c0}

텍스트 문자열입니다. 비어 있거나 유효한 상대 폴더 경로이거나 이미지 서버에서 액세스할 수 있는 유효한 절대 경로여야 합니다.

## 기본값 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

정의되지 않은 경우 `default::RootPath`에서 상속됩니다. 를 정의했지만 비어 있으면 소스 파일 루트 경로에 기여하지 않습니다.

## 참조 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),   [규칙 세트::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [소스 데이터 관리](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
