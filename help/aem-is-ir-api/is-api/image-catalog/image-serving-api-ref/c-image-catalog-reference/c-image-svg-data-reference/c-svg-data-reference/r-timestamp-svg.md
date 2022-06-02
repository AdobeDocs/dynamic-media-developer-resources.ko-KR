---
description: 타임스탬프
solution: Experience Manager
title: 타임스탬프
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# 타임스탬프{#timestamp}

If `attribute::UseLastModified` 이 설정되면, `catalog::TimeStamp` 값은 HTTP 응답에서 마지막 수정 HTTP 헤더로 반환됩니다. Last-Modified 헤더는 항상 정적 컨텐츠에 대해 반환되지만, `attribute::UseLastModified` 가 설정되지 않았습니다.

이미지 및 SVG 컨텐츠의 경우, `catalog::TimeStamp` 카탈로그 기반 캐시 유효성 검사에도 사용됩니다(참조 [특성::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## 속성 {#section-2298a384b5cb43929542655c5a49beb2}

Java 형식의 날짜/시간 값. 1970년 1월 1일 자정 이후 정수(밀리초) 또는 다음 형식 중 하나가 있는 날짜/시간 문자열 값일 수 있습니다.

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* 는 0 - 23 범위에 있습니다.

*`zzz`* 는 &#39;GMT&#39; 또는 &#39;PST&#39;와 같은 3~4자의 시간대 코드입니다. 시간대 코드의 일광 절약 시간제가 사용됩니다. 예를 들어, 태평양 표준시(PST)와 태평양 일광 절약 시간제의 경우 &#39;PDT&#39;(PDT))가 있습니다.

*`offset`* 는 시간대 오프셋(시간 또는 시간 단위)입니다. `hours:minutes`를 반환합니다. 예를 들어 &#39;PDT&#39;는 &#39;GMT -7&#39;와 같습니다.

문자열 형식의 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바르게 지정되지 않으면 해당 값은 무시되고 수정 시간은 `*`카탈로그`*.ini` 파일이 대신 사용됩니다.

## 기본값 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 필드가 비어 있거나 없는 경우.

## 참조 {#section-c42a427aa4794c548408dc4de028d578}

[속성::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [특성::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
