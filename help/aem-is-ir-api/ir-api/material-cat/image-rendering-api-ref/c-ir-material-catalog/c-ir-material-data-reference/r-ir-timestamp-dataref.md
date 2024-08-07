---
title: 타임스탬프
description: 파일 수정 타임스탬프. 이 카탈로그 레코드에 첨부된 이미지 및/또는 데이터 파일을 마지막으로 수정한 날짜/시간을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# 타임스탬프{#timestamp}

파일 수정 타임스탬프. 이 카탈로그 레코드에 첨부된 이미지 및/또는 데이터 파일을 마지막으로 수정한 날짜/시간을 지정합니다.

`attribute::UseLastModified`이(가) 설정되면 모든 자료의 가장 최근 값 `catalog::TimeStamp` 및 `vignette::TimeStamp`과(와) 요청에 포함된 비네팅이 HTTP 응답에서 마지막으로 수정된 헤더로 반환됩니다.

>[!NOTE]
>
>이 카탈로그 레코드에 첨부된 이미지 또는 데이터 파일의 실제 파일 시간은 이 용도로 사용되지 않습니다.

`catalog::TimeStamp`은(는) 카탈로그 기반 캐시 유효성 검사에도 사용됩니다([attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md) 참조).

## 속성 {#section-42f09e375e72492b87a3a486da7df808}

Java™ 형식의 날짜/시간 값입니다. 이 값은 자정, 1970년 1월 1일(UTC/GMT) 이후의 정수(밀리초) 또는 다음 형식 중 하나의 날짜/시간 문자열 값일 수 있습니다.

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]*&#x200B;은(는) 0~23 범위에 있습니다.
* *[!DNL zzz]*&#x200B;은(는) &#39;GMT&#39; 또는 &#39;PST&#39;와 같은 3~4자 표준 시간대 코드입니다. 일광 절약 시간제는 시간대 코드에서 고려해야 합니다. 예를 들어 태평양 표준시간의 경우 &#39;PST&#39;와 태평양 일광 절약 시간의 경우 &#39;PDT&#39;가 있습니다.
* *[!DNL offset]*&#x200B;은(는) GMT를 기준으로 한 시간대 오프셋(시간 또는 시간:분 단위)입니다. 예를 들어 &#39;PDT&#39;는 &#39;GMT -7&#39;과 같습니다.

문자열 형식의 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바르지 않으면 이 값은 무시되고 대신 *catalog*.ini 파일의 수정 시간이 사용됩니다.

## 기본값 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp`은(는) 비어 있거나 없는 필드입니다.

## 참조 {#section-876f1d1b50dc4501b605820015a29451}

[특성::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [특성::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [특성::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [비네팅::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
