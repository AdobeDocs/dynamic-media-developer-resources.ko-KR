---
description: 서버 캐시 유효성 검사 정책. 서버측 캐시 항목의 유효성을 검사할 시기를 지정합니다.
seo-description: 서버 캐시 유효성 검사 정책. 서버측 캐시 항목의 유효성을 검사할 시기를 지정합니다.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

서버 캐시 유효성 검사 정책. 서버측 캐시 항목의 유효성을 검사할 시기를 지정합니다.

만료 기반의 유효성 검사를 통해 소스 자료와 비네팅을 정기적으로 확인하여 내용이 변경되었는지 확인합니다. 카탈로그 기반 유효성 검사를 사용하면 `catalog::TimeStamp` 값이 변경된 후에만 소스 이미지가 확인됩니다.

재료 및 비네팅 카탈로그를 모두 사용하는 경우 카탈로그 기반 유효성 검사가 권장됩니다. 비네팅이 경로별로 이미지 렌더링 요청에서 직접 참조되는 경우 만료 기반 유효성 검사를 사용해야 합니다.

## 속성 {#section-46e13cb341eb442c86e0d8292de23ea0}

열거형. 0을 클릭하여 만료 기반 유효성 검사를 선택합니다. 1 - 카탈로그 기반 캐시 유효성 검사를 선택합니다.

## 기본값 {#section-e09f3af8b6b3497d963199988dc5345d}

정의되지 않았거나 비어 있는 경우 `default::CacheValidationPolicy`에서 상속됩니다.

## 참조 {#section-b374e4d908e24af8995b2b376ca1be8b}

[카탈로그::타임스탬프](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
