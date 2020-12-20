---
description: 기본 이미지 수정 타임스탬프. 카탈로그 타임스탬프에 대한 기본값을 제공합니다.
seo-description: 기본 이미지 수정 타임스탬프. 카탈로그 타임스탬프에 대한 기본값을 제공합니다.
seo-title: 타임스탬프
solution: Experience Manager
title: 타임스탬프
topic: Scene7 Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# 타임스탬프{#timestamp}

기본 이미지 수정 타임스탬프. 카탈로그::TimeStamp의 기본값을 제공합니다.

지정하지 않으면 서버는 이 [!DNL *`catalog`*.ini] 파일의 수정 날짜/시간을 사용합니다.

## 속성 {#section-647066e62ce44a84b627fdd0b2f7cfec}

날짜/시간 값입니다. 1970년 1월 1일 자정 이후 정수(밀리초) 또는 다음 형식 중 하나를 사용하여 날짜/시간 문자열 값을 지정할 수 있습니다.

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* 0에서 23 사이의 범위에 있습니다.

*`zzz`* 은 또는 `GMT` 과 같은 3 또는 4자 표준 시간대 코드입니다 `PST`. 일광 절약 시간은 시간대 코드(예:태평양 표준시 기준 시점의 경우 `PST`, 태평양 일광 절약 시간의 경우 `PDT` 비교).

*`offset`* 은 GMT를 기준으로 시간 또는 시간:분 단위 시간대 오프셋입니다. 예를 들어 `PDT`는 `GMT -7`와 같습니다.

문자열 형식 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바로 지정되지 않으면 무시되고 [!DNL *`catalog`*.ini] 파일의 수정 시간이 대신 사용됩니다.

## 기본값 {#section-ac465313c97943ed97d41ea852329177}

비어 있거나 정의되지 않은 경우 서버는 이 ` *`catalog`*.ini` 파일의 파일 수정 시간을 사용합니다.

## 참조 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[카탈로그::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [속성::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [속성::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
