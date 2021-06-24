---
description: 워터마크 선택기. 워터마크 이미지 또는 템플릿으로 사용할 카탈로그 레코드의 카탈로그 ID를 지정합니다.
solution: Experience Manager
title: 워터마크
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---

# 워터마크{#watermark}

워터마크 선택기. 워터마크 이미지 또는 템플릿으로 사용할 카탈로그::Id를 지정합니다.

지정된 경우 서버는 모든 이미지 요청에 대해 요청된 이미지 데이터에 워터마크를 적용합니다( `req=img`).

## 속성 {#section-fad6ffff4c5f4b5c8010281bc1377055}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그의 유효한 `Catalog::Id` 값이어야 합니다(또는 [!DNL default.ini]에 지정된 경우 기본 카탈로그에서).

## 기본값 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

정의되지 않은 경우 `default::Watermark`에서 상속됩니다. `default::Watermark` 이 정의되어 있지만 비어 있으면 이 이미지 카탈로그에 대해 워터마킹(watermarking)이 적용되지 않습니다.

## 참조 {#section-f15dbe31013849828d78588742dde58e}

[카탈로그::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
