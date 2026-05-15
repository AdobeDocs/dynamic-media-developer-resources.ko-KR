---
title: CacheValidationPolicy
description: 서버 캐시 유효성 검사 정책입니다. 서버측 캐시 항목의 유효성을 검사하는 시기를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
TQID: 'https://experienceleague.adobe.com/8WipxBM2HngJP5f8LOJmFPA5jZTyJt6Q5P9mZnzDPsY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

서버 캐시 유효성 검사 정책입니다. 서버측 캐시 항목의 유효성을 검사하는 시기를 지정합니다.

만료 기반 유효성 검사를 통해 소스 자료 및 비네팅이 변경되었는지 정기적으로 확인합니다. 카탈로그 기반 유효성 검사를 사용하면 `catalog::TimeStamp` 값이 변경된 후에만 소스 이미지를 검사합니다.

자료 카탈로그와 비네팅 카탈로그를 모두 사용할 경우에는 카탈로그 기반 유효성 검사가 권장됩니다. 이미지 렌더링 요청에서 경로를 통해 직접 비네팅을 참조하는 경우 만료 기반 유효성 검사를 사용해야 합니다.

## 속성 {#section-46e13cb341eb442c86e0d8292de23ea0}

열거형. 만료 기반 유효성 검사를 선택하려면 0을 사용합니다. 1 - 카탈로그 기반 캐시 유효성 검사를 선택합니다.

## 기본값 {#section-e09f3af8b6b3497d963199988dc5345d}

정의되지 않았거나 비어 있는 경우 `default::CacheValidationPolicy`에서 상속됩니다.

## 참조 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
