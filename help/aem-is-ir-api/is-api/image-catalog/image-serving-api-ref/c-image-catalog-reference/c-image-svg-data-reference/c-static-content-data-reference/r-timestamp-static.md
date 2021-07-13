---
description: 타임스탬프
solution: Experience Manager
title: 타임스탬프
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c47b14d-b629-474d-952a-b09e1b1162b4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# 타임스탬프{#timestamp}

`attribute::UseLastModified` 이 설정되면 `catalog::TimeStamp` 값이 HTTP 응답에서 Last-Modified HTTP 헤더로 반환됩니다. `attribute::UseLastModified` 이 설정되지 않은 경우에도 정적 컨텐츠에 대해 Last-Modified 헤더가 항상 반환됩니다.

이미지 및 SVG 콘텐츠의 경우 `catalog::TimeStamp`도 카탈로그 기반 캐시 유효성 검사에 사용됩니다( ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)` 참조).

## 속성 {#section-2298a384b5cb43929542655c5a49beb2}

Java 형식의 날짜/시간 값. 1970년 1월 1일 자정 이후 정수(밀리초) 또는 다음 형식 중 하나가 있는 날짜/시간 문자열 값일 수 있습니다.

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* 는 0 - 23 범위에 있습니다.

*`zzz`* 는 &#39;GMT&#39; 또는 &#39;PST&#39;와 같은 3~4자의 시간대 코드입니다. 시간대 코드의 일광 절약 시간제가 사용됩니다. 예를 들어, 태평양 표준시(PST)와 태평양 일광 절약 시간제의 경우 &#39;PDT&#39;(PDT))가 있습니다.

*`offset`* 는 GMT를 기준으로 하는 시간대 오프셋(시간 단위) `hours:minutes`입니다. 예를 들어 &#39;PDT&#39;는 &#39;GMT -7&#39;와 같습니다.

문자열 형식의 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바르게 지정되지 않으면 이 값은 무시되고 `*`catalog`*.ini` 파일의 수정 시간이 대신 사용됩니다.

## 기본값 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 필드가 비어 있거나 없는 경우.

## 참조 {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
