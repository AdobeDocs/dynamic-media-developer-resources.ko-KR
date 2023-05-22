---
description: 기본 이미지 수정 타임스탬프. 카탈로그 타임스탬프의 기본값을 제공합니다.
solution: Experience Manager
title: 타임스탬프
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# 타임스탬프{#timestamp}

기본 이미지 수정 타임스탬프. catalog::TimeStamp에 대한 기본값을 제공합니다.

지정하지 않으면 서버는 수정 날짜/시간을 사용합니다 [!DNL *`catalog`*.ini] 파일.

## 속성 {#section-647066e62ce44a84b627fdd0b2f7cfec}

날짜/시간 값. 는 1970년 1월 1일 자정, UTC/GMT 이후의 정수(밀리초) 또는 다음 형식 중 하나의 날짜/시간 문자열 값일 수 있습니다.

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* 은(는) 0에서 23 사이의 범위에 있습니다.

*`zzz`* 는 다음과 같은 3 또는 4자 표준 시간대 코드입니다. `GMT` 또는 `PST`. 일광 절약 시간제는 시간대 코드에서 고려해야 합니다(예: `PST` (태평양 표준시 기준), `PDT` - 태평양 일광 절약 시간제).

*`offset`* 는 GMT를 기준으로 한 시간대 오프셋(시간 또는 시간:분 단위)입니다. 예를 들어, `PDT` 은(는) 와 동일합니다. `GMT -7`.

문자열 형식의 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바르지 않으면 이 값은 무시되고 의 수정 시간이 적용됩니다. [!DNL *`catalog`*.ini] 파일이 대신 사용됩니다.

## 기본값 {#section-ac465313c97943ed97d41ea852329177}

비어 있거나 정의되지 않은 경우 서버는 이 파일의 파일 수정 시간을 사용합니다 `*`카탈로그`*.ini` 파일.

## 참조 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
