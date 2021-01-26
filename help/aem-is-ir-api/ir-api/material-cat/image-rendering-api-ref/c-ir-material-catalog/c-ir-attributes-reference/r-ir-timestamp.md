---
description: 기본 수정 타임스탬프. 카탈로그 타임스탬프 및 비네팅 타임스탬프에 대한 기본값을 제공합니다. 지정하지 않으면 서버는 이 catalog.ini 파일의 수정 날짜/시간을 사용합니다.
seo-description: 기본 수정 타임스탬프. 카탈로그 타임스탬프 및 비네팅 타임스탬프에 대한 기본값을 제공합니다. 지정하지 않으면 서버는 이 catalog.ini 파일의 수정 날짜/시간을 사용합니다.
seo-title: 타임스탬프
solution: Experience Manager
title: 타임스탬프
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# 타임스탬프{#timestamp}

기본 수정 타임스탬프. 카탈로그::TimeStamp 및 비네팅::TimeStamp의 기본값을 제공합니다. 지정하지 않으면 서버는 이 catalog.ini 파일의 수정 날짜/시간을 사용합니다.

## 속성 {#section-910e2562b41c47b78ee6216deeabbbd5}

Java 형식의 날짜/시간 값. 1970년 1월 1일 자정 이후 정수(밀리초) 또는 다음 형식 중 하나를 사용하여 날짜/시간 문자열 값을 지정할 수 있습니다.

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* 0에서 23 사이의 범위에 있습니다.

*[!DNL zzz]* 은 &#39;GMT&#39; 또는 &#39;PST&#39;와 같은 3 또는 4자 표준 시간대 코드입니다. 일광 절약 시간은 시간대 코드(예: 태평양 표준시의 경우 &#39;PST&#39;, 태평양 일광 절약 시간제의 경우 &#39;PDT&#39;)에서 계산되어야 합니다.

*[!DNL offset]* 은 GMT를 기준으로 시간 또는 시간:분 단위 시간대 오프셋입니다. 예를 들어 &#39;PDT&#39;는 &#39;GMT -7&#39;와 같습니다.

문자열 형식 날짜/시간 값의 모든 요소가 있어야 합니다. 날짜/시간 값의 형식이 올바로 지정되지 않으면 무시되고 [!DNL *[!DNL catalog]*.ini] 파일의 수정 시간이 대신 사용됩니다.

## 기본값 {#section-65fb29a9ea2044df8cb9fe295eb14872}

비어 있거나 정의되지 않은 경우 서버는 이 [!DNL *[!DNL catalog]*.ini] 파일의 파일 수정 시간을 사용합니다.

## 참조 {#section-764188f9b1734ad1a6270f5fecd28532}

[카탈로그::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [비네팅::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [속성::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [속성::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
