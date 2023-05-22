---
title: CacheValidationPolicy
description: 서버 캐시 유효성 검사 정책입니다. 서버측 캐시 항목의 유효성을 검사하는 시기를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

서버 캐시 유효성 검사 정책입니다. 서버측 캐시 항목의 유효성을 검사하는 시기를 지정합니다.

만료 기반 유효성 검사를 사용하면 소스 이미지가 변경되었는지 정기적으로 확인합니다. 카탈로그 기반 유효성 검사를 사용하면 소스 이미지는 `catalog::TimeStamp` 값이 변경되었습니다.

이미지 카탈로그를 사용하는 경우 카탈로그 기반 유효성 검사가 권장됩니다. 이미지 카탈로그를 사용하지 않고 이미지를 직접 참조할 때 만료 기반 유효성 검사를 사용해야 합니다.

## 속성 {#section-650cbddd81a24c3b8b70479248a45dc9}

열거형. 만료 기반 유효성 검사를 선택하려면 0을 선택하고, 카탈로그 기반 캐시 유효성 검사를 선택하려면 1을 선택합니다.

## 기본값 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

상속 위치 `default::CacheValidationPolicy` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
