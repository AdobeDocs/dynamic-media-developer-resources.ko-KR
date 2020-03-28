---
description: 기본 이미지 수정 타임스탬프. 카탈로그 타임스탬프의 기본값을 제공합니다.
seo-description: 기본 이미지 수정 타임스탬프. 카탈로그 타임스탬프의 기본값을 제공합니다.
seo-title: 타임스탬프
solution: Experience Manager
title: 타임스탬프
topic: Scene7 Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

기본 이미지 수정 타임스탬프. 카탈로그::TimeStamp의 기본값을 제공합니다.

지정하지 않으면 서버는 이 [!DNL *`catalog`*.ini] 파일의 수정 날짜/시간을 사용합니다.

## 속성 {#section-647066e62ce44a84b627fdd0b2f7cfec}

날짜/시간 값. 1970년 1월 1일 자정 이후의 정수(밀리초) 또는 다음 형식 중 하나를 포함하는 날짜/시간 문자열 값일 수 있습니다.

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*:GMT *`ss`* GMT *`offset`*

*`hh`* 가 0에서 23 사이의 범위에 있습니다.

*`zzz`* 은 `GMT` 또는 와 같은 3 또는 4자 표준 시간대 `PST`코드입니다. 일광 절약 시간은 시간대 코드(예: 태평양 표준시와 태평양 일광 절약 시간제 비교)에서 `PST` `PDT` 계산되어야 합니다.

*`offset`* 은 GMT를 기준으로 시간 또는 시간:분 단위의 표준 시간대 오프셋입니다. 예를 들어, 는 `PDT` 와 `GMT -7`같습니다.

문자열 형식 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바로 지정되지 않으면 이 값은 무시되고 [!DNL *`catalog`*.ini] 파일의 수정 시간이 대신 사용됩니다.

## 기본값 {#section-ac465313c97943ed97d41ea852329177}

비어 있거나 정의되지 않은 경우 서버는 이 ` *`카탈로그`*.ini` 파일의 파일 수정 시간을 사용합니다.

## 참조 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)[attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
