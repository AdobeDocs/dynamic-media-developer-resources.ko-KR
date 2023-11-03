---
title: 마지막 수정 날짜 사용
description: 마지막으로 수정된 응답 헤더를 활성화합니다. 이미지 렌더링에서 내보낸 캐시 가능한 HTTP 응답에 마지막 수정 헤더 포함을 활성화하거나 비활성화합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 1%

---

# 마지막 수정 날짜 사용{#uselastmodified}

마지막으로 수정된 응답 헤더를 활성화합니다. 이미지 렌더링에서 내보낸 캐시 가능한 HTTP 응답에 마지막 수정 헤더 포함을 활성화하거나 비활성화합니다.

서버에서 가장 최근 을 사용합니다. `vignette::TimeStamp` 및 `catalog::TimeStamp` Last-Modified 헤더 값으로 응답에 포함된 모든 비네팅 및 자재 카탈로그/카탈로그 레코드의 값.

Akamai와 같은 분산 캐싱 네트워크가 etag 헤더를 지원하지 않는 경우에만 활성화해야 합니다.

>[!NOTE]
>
>여러 이미지 제공/렌더링 호스트가 포함된 로드 밸런싱된 환경에서 마지막으로 수정된 헤더를 사용할 때 주의해야 합니다. 어떤 이유로든 서버에 동일한 카탈로그 항목에 대한 다른 타임스탬프가 있는 경우 클라이언트 캐싱이 중단되고 서버 로드가 증가할 수 있습니다. 이러한 상황은 다음과 같이 발생할 수 있습니다.

* `catalog::TimeStamp`, `vignette::TimeStamp`, 또는 `attribute::TimeStamp` 가 정의되지 않았으므로 의 수정 시간이 [!DNL catalog.ini] 파일은 의 기본값으로 사용됩니다. `catalog::TimeStamp`.

* 네트워크 마운트를 통해 자료 카탈로그 파일을 공유하는 대신 각 서버는 로컬 파일 시스템에 카탈로그 파일의 자체 인스턴스를 가지고 있습니다.
* 동일한 인스턴스 2개 이상 [!DNL catalog.ini] 파일의 파일 수정 날짜가 다릅니다. 파일을 잘못 복사했기 때문일 수 있습니다.

## 속성 {#section-453952244193452caccfaf7f601007c1}

플래그. 비활성화하려면 0을 사용하고, 마지막으로 수정한 HTTP 헤더를 활성화하려면 1을 사용합니다.

## 기본값 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

상속 위치 `default::UseLastModified` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [비네팅::타임스탬프](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
