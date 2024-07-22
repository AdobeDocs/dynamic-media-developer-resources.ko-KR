---
description: 워터마크 선택기. 워터마크 이미지 또는 템플릿으로 사용할 카탈로그 레코드의 카탈로그 ID를 지정합니다.
solution: Experience Manager
title: 워터마크
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# 워터마크{#watermark}

워터마크 선택기. 워터마크 이미지 또는 템플릿으로 사용할 카탈로그 레코드의 catalog::Id를 지정합니다.

지정하면 서버에서 모든 이미지 요청(`req=img`)에 대해 요청된 이미지 데이터에 워터마크를 적용합니다.

## 속성 {#section-fad6ffff4c5f4b5c8010281bc1377055}

텍스트 문자열입니다. 지정하면 이 이미지 카탈로그(또는 [!DNL default.ini]에 지정된 경우 기본 카탈로그)에서 올바른 `Catalog::Id` 값이어야 합니다.

## 기본값 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

정의되지 않은 경우 `default::Watermark`에서 상속됩니다. `default::Watermark`이(가) 정의되어 있더라도 비어 있으면 이 이미지 카탈로그에 대해 워터마크가 적용되지 않습니다.

## 참조 {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
