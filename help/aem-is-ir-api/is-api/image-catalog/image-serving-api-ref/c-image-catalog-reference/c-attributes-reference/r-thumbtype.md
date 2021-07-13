---
description: 기본 축소판 그림 유형. 특정 카탈로그 레코드에 올바른 카탈로그 ThumbType 값이 없는 경우 축소판 유형에 대한 기본값을 제공합니다.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac29ac3a-8c6b-4c87-954f-37d1ddec76f5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# ThumbType{#thumbtype}

기본 축소판 그림 유형. 특정 카탈로그 레코드에 올바른 카탈로그:ThumbType 값이 없는 경우 축소판 유형에 대한 기본값을 제공합니다.

축소판 요청( `req=tmb`)에만 사용됩니다.

## 속성 {#section-ae0babfe3c8e4c8ebe0124bc55051265}

열거형. 허용되는 값은 각각 *`crop`*, *`fit`* 및 *`texture`* 축소판 유형에 대해 1, 2 및 3입니다.

## 기본값 {#section-0237fcae4f304c5b876fceaa839b6b05}

정의되지 않았거나 비어 있는 경우 `default::ThumbType`에서 상속됩니다.

## 참조 {#section-986c97470c494bfd8f179cecf8cc3ccc}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)
