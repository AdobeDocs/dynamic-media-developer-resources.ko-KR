---
description: 기본 이미지 수정 타임스탬프. 카탈로그 타임스탬프의 기본값을 제공합니다.
solution: Experience Manager
title: 타임스탬프
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# 타임스탬프{#timestamp}

기본 이미지 수정 타임스탬프. 카탈로그에 대한 기본값을 제공합니다.:TimeStamp.

지정하지 않으면 서버는 이 [!DNL *`catalog`*.ini] 파일의 수정 날짜/시간을 사용합니다.

## 속성 {#section-647066e62ce44a84b627fdd0b2f7cfec}

날짜/시간 값. 1970년 1월 1일 자정 이후 정수(밀리초) 또는 다음 형식 중 하나가 있는 날짜/시간 문자열 값일 수 있습니다.

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* 는 0~23 범위에 있습니다.

*`zzz`* 는 또는 와 같은 3 또는 4자리 시간대  `GMT` 코드입니다  `PST`. 일광 절약 시간제가 시간대 코드에서 계산되어야 합니다(예:`PST`(태평양 표준시) 및 `PDT`(태평양 일광 절약 시간제의 경우).

*`offset`* 은 GMT를 기준으로 시간 또는 시간:분 단위 시간대 오프셋입니다. 예를 들어 `PDT`은 `GMT -7`에 해당합니다.

문자열 형식의 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바르게 지정되지 않으면 이 값은 무시되고 [!DNL *`catalog`*.ini] 파일의 수정 시간이 대신 사용됩니다.

## 기본값 {#section-ac465313c97943ed97d41ea852329177}

비어 있거나 정의되지 않은 경우 서버는 이 `*`catalog`*.ini` 파일의 파일 수정 시간을 사용합니다.

## 참조 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [속성::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [속성::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
