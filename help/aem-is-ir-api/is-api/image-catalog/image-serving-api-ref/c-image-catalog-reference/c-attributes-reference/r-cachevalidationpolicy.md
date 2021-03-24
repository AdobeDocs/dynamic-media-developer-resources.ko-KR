---
description: 서버 캐시 유효성 검사 정책. 서버측 캐시 항목의 유효성을 검사할 시기를 지정합니다.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

서버 캐시 유효성 검사 정책. 서버측 캐시 항목의 유효성을 검사할 시기를 지정합니다.

만료 기반 유효성 검사를 통해 소스 이미지가 변경되었는지 주기적으로 확인됩니다. 카탈로그 기반 유효성 검사를 사용하면 `catalog::TimeStamp` 값이 변경된 후에만 소스 이미지가 확인됩니다.

이미지 카탈로그를 사용할 때는 카탈로그 기반 유효성 검사가 권장됩니다. 이미지 카탈로그를 사용하지 않고 이미지를 직접 참조하는 경우 만료 기반 유효성 검사를 사용해야 합니다.

## 속성 {#section-650cbddd81a24c3b8b70479248a45dc9}

열거형. 만료 기반 유효성 검사를 선택하려면 0, 카탈로그 기반 캐시 유효성 검사를 선택하려면 1.

## 기본값 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

정의되지 않았거나 비어 있는 경우 `default::CacheValidationPolicy`에서 상속됩니다.

## 참조 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[카탈로그::타임스탬프](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
