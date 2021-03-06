---
description: 수정 타임스탬프. 이 비네팅을 마지막으로 수정한 날짜/시간을 지정합니다.
solution: Experience Manager
title: 타임스탬프
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 타임스탬프{#timestamp}

수정 타임스탬프. 이 비네팅을 마지막으로 수정한 날짜/시간을 지정합니다.

If `attribute::UseLastModified` 이 설정되고, 가장 최근 `vignette::TimeStamp` 및 `catalog::TimeStamp`비네트의 값과 요청에 관련된 모든 자료가 HTTP 응답에서 마지막 수정 헤더로 반환됩니다.

>[!NOTE]
>
>비네팅 파일의 실제 파일 시간은 이 용도로 사용되지 않습니다.

`catalog::TimeStamp` 카탈로그 기반 캐시 유효성 검사에도 사용됩니다(참조 [특성::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## 속성 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java 형식의 날짜/시간 값. 1970년 1월 1일 자정 이후 정수(밀리초) 또는 다음 형식 중 하나가 있는 날짜/시간 문자열 값일 수 있습니다.

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* 는 0~23 범위에 있습니다.
* *[!DNL zzz]* 는 &#39;GMT&#39; 또는 &#39;PST&#39;와 같은 3 또는 4자의 시간대 코드입니다. 일광 절약 시간제는 시간대 코드(예: 태평양 표준시의 경우 &#39;PST&#39;, 태평양 일광 절약 시간제의 경우 &#39;PDT&#39;)에서 계산되어야 합니다.
* *[!DNL offset]* 은 GMT를 기준으로 시간 또는 시간:분 단위 시간대 오프셋입니다. 예를 들어 &#39;PDT&#39;는 &#39;GMT -7&#39;와 같습니다.

문자열 형식의 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바르게 지정되지 않으면 이 값은 무시되고 [!DNL *[!DNL catalog]*.ini] 파일이 대신 사용됩니다.

## 기본값 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` 필드가 비어 있거나 없습니다.

## 참조 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[속성::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [카탈로그::타임스탬프](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
