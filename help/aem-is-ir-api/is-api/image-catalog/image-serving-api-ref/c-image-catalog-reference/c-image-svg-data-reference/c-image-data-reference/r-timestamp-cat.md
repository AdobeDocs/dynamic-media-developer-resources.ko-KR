---
title: 타임스탬프
description: '''attribute::UseLastModified''가 설정되면 ''catalog::TimeStamp'' 값이 HTTP 응답에 Last-Modified HTTP 헤더로 반환됩니다.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
TQID: 'https://experienceleague.adobe.com/Am7JECwqMWbky2JrHKqZV1BJ7ef06JP9Sy-g9uUo8tw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 1%

---

# 타임스탬프{#timestamp}

`attribute::UseLastModified`이(가) 설정되면 HTTP 응답에서 `catalog::TimeStamp` 값이 마지막으로 수정된 HTTP 헤더로 반환됩니다. `attribute::UseLastModified`이(가) 설정되지 않은 경우에도 정적 콘텐츠에 대해 Last-Modified 헤더가 항상 반환됩니다.

이미지 및 SVG 컨텐츠의 경우 카탈로그 기반 캐시 유효성 검사에 `catalog::TimeStamp`도 사용됩니다([attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md) 참조).

## 속성 {#section-2298a384b5cb43929542655c5a49beb2}

Java 형식의 날짜/시간 값입니다. 는 자정, 1970년 1월 1일, UTC/GMT 이후의 정수(밀리초) 또는 다음 형식 중 하나의 날짜/시간 문자열 값일 수 있습니다.

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`*&#x200B;은(는) 0 - 23 범위에 있습니다.

*`zzz`*&#x200B;은(는) &#39;GMT&#39; 또는 &#39;PST&#39;와 같은 3~4자 표준 시간대 코드입니다. 시간대 코드의 일광 절약 시간제 계정입니다. 예를 들어 태평양 표준시간의 경우 &#39;PST&#39;와 태평양 일광 절약 시간제의 경우 &#39;PDT&#39;가 다릅니다.

*`offset`*&#x200B;은(는) GMT를 기준으로 한 시간대 오프셋(시간 또는 `hours:minutes`)입니다. 예를 들어 &#39;PDT&#39;는 &#39;GMT -7&#39;과 같습니다.

문자열 형식의 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바르지 않으면 무시됩니다. 대신 `*`catalog`*.ini` 파일의 수정 시간이 사용됩니다.

## 기본값 {#section-0cbf801401ff4857bdda168fd12358af}

필드가 비어 있거나 없는 경우 `attribute::TimeStamp`.

## 참조 {#section-c42a427aa4794c548408dc4de028d578}

[특성::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [특성::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [특성::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
