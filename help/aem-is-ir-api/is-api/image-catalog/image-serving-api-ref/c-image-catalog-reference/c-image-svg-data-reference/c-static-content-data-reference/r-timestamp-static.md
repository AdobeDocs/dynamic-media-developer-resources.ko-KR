---
description: 널
seo-description: 널
seo-title: 타임스탬프
solution: Experience Manager
title: 타임스탬프
topic: Scene7 Image Serving - Image Rendering API
uuid: fd60e5db-9219-41a8-947f-0d497b39e727
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# TimeStamp{#timestamp}

이 `attribute::UseLastModified` 값을 설정하면 HTTP 응답에서 마지막 수정 HTTP 헤더로 값이 반환됩니다 `catalog::TimeStamp` . 마지막으로 수정한 헤더는 설정되지 않은 경우에도 정적 컨텐츠에 대해 항상 반환됩니다. `attribute::UseLastModified`

이미지 및 SVG 컨텐츠의 경우 카탈로그 기반 캐시 검증에도 `catalog::TimeStamp` 사용됩니다(참조 ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## 속성 {#section-2298a384b5cb43929542655c5a49beb2}

Java 형식의 날짜/시간 값입니다. 1970년 1월 1일 자정 이후의 정수(밀리초) 또는 다음 형식 중 하나가 있는 날짜/시간 문자열 값일 수 있습니다.

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*:GMT *`ss`* GMT *`offset`*

*`hh`* 는 0 - 23 범위에 있습니다.

*`zzz`* 은 &#39;GMT&#39; 또는 &#39;PST&#39;와 같은 3 또는 4자 표준 시간대 코드입니다. 시간대 코드의 일광 절약 시간제에 대한 계정입니다. 예를 들어 태평양 표준시(PST)와 태평양 일광 절약 시간제의 경우 &#39;PDT&#39;(PDT) 등이 있습니다.

*`offset`* 은 시간 또는 GMT를 기준으로 `hours:minutes`하는 시간대 오프셋입니다. 예를 들어 &#39;PDT&#39;는 &#39;GMT -7&#39;와 같습니다.

문자열 형식 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바로 지정되지 않으면 ` *`카탈로그`*.ini` 파일의 수정 시간이 무시됩니다.

## 기본값 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` if the field is empty or not present.

## 참조 {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified,](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)[attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
