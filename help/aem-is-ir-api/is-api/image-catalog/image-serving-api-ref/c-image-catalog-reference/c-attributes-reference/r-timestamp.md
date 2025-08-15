---
title: 타임스탬프
description: 기본 이미지 수정 타임스탬프. 카탈로그 타임스탬프의 기본값을 제공합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# 타임스탬프{#timestamp}

기본 이미지 수정 타임스탬프. catalog::TimeStamp에 대한 기본값을 제공합니다.

지정하지 않으면 서버에서 이 [!DNL *`catalog`*.ini] 파일의 수정 날짜/시간을 사용합니다.

## 속성 {#section-647066e62ce44a84b627fdd0b2f7cfec}

날짜/시간 값. 이 값은 자정, 1970년 1월 1일(UTC/GMT) 이후의 정수(밀리초) 또는 다음 형식 중 하나의 날짜/시간 문자열 값일 수 있습니다.

날짜/시간 값 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

날짜/시간 값 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

시간 값 *`hh`*&#x200B;이(가) 0~23 범위에 있습니다.

시간 값 *`zzz`*&#x200B;은(는) `GMT` 또는 `PST`과(와) 같은 3~4자 표준 시간대 코드입니다. 일광 절약 시간제는 시간대 코드에서 계산해야 합니다(예: 태평양 표준시간의 경우 `PST`, 태평양 일광 절약 시간제의 경우 `PDT`).

시간 값 *`offset`*&#x200B;은(는) GMT를 기준으로 한 시간 또는 시간:minutes 단위의 시간대 오프셋입니다. 예를 들어 `PDT`은(는) `GMT -7`과(와) 같습니다.

문자열 형식의 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바르지 않으면 이 값이 무시되고 대신 [!DNL *`catalog`*.ini] 파일의 수정 시간이 사용됩니다.

## 기본값 {#section-ac465313c97943ed97d41ea852329177}

비어 있거나 정의되지 않은 경우 서버는 이 `*`카탈로그`*.ini` 파일의 파일 수정 시간을 사용합니다.

## 참조 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[카탈로그::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [특성::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [특성::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
