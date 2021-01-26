---
description: 타임스탬프
solution: Experience Manager
title: 타임스탬프
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9ce5e42e-573a-4e1c-97d4-98888e16ca56
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# 타임스탬프{#timestamp}

`attribute::UseLastModified`이(가) 설정된 경우 HTTP 응답에서 마지막으로 수정한 HTTP 헤더로 `catalog::TimeStamp` 값이 반환됩니다. `attribute::UseLastModified`이(가) 설정되어 있지 않더라도 정적 콘텐츠에 대해 마지막으로 수정한 헤더가 항상 반환됩니다.

이미지 및 SVG 내용의 경우 카탈로그 기반 캐시 유효성 검사에도 `catalog::TimeStamp`이(가) 사용됩니다( ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)` 참조).

## 속성 {#section-2298a384b5cb43929542655c5a49beb2}

Java 형식의 날짜/시간 값. 1970년 1월 1일 자정 이후 정수(밀리초) 또는 다음 형식 중 하나를 사용하여 날짜/시간 문자열 값을 지정할 수 있습니다.

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* 는 0 - 23 범위의 값입니다.

*`zzz`* 은 &#39;GMT&#39; 또는 &#39;PST&#39;와 같은 3 또는 4문자 표준 시간대 코드입니다. 시간대 코드에서 일광 절약 시간을 고려합니다. 예를 들어 태평양 표준시의 경우 &#39;PST&#39;, 태평양 일광 절약 시간제의 경우 &#39;PDT&#39; 등

*`offset`* 은 시간 단위 또는 GMT를 기준으로 하는  `hours:minutes`시간대 오프셋입니다. 예를 들어 &#39;PDT&#39;는 &#39;GMT -7&#39;와 같습니다.

문자열 형식 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바로 지정되지 않으면 무시되고 `*`catalog`*.ini` 파일의 수정 시간이 대신 사용됩니다.

## 기본값 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 필드가 비어 있거나 없는 경우

## 참조 {#section-c42a427aa4794c548408dc4de028d578}

[속성::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [속성::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [속성::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
