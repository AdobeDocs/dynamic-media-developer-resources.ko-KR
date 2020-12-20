---
description: 마지막으로 수정한 응답 헤더를 활성화합니다. 이미지 렌더링에서 방출하는 캐시 가능한 HTTP 응답에 마지막으로 수정한 헤더 포함을 활성화하거나 비활성화합니다.
seo-description: 마지막으로 수정한 응답 헤더를 활성화합니다. 이미지 렌더링에서 방출하는 캐시 가능한 HTTP 응답에 마지막으로 수정한 헤더 포함을 활성화하거나 비활성화합니다.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

마지막으로 수정한 응답 헤더를 활성화합니다. 이미지 렌더링에서 방출하는 캐시 가능한 HTTP 응답에 마지막으로 수정한 헤더 포함을 활성화하거나 비활성화합니다.

서버는 응답에 포함된 모든 비네팅 및 자료 카탈로그/카탈로그 레코드의 최신 `vignette::TimeStamp` 및 `catalog::TimeStamp` 값을 마지막 수정 머리글 값으로 사용합니다.

Akamai와 같은 분산 캐싱 네트워크가 Tag 헤더를 지원하지 않는 경우에만 활성화되어야 합니다.

>[!NOTE]
>
>여러 이미지 제공/렌더링 호스트가 포함된 로드 밸런싱된 환경에서 마지막으로 수정한 헤더를 사용할 때는 주의해야 합니다. 서버에 동일한 카탈로그 항목에 대한 타임스탬프가 다른 경우 클라이언트 캐싱이 실패하여 서버 로드가 증가할 수 있습니다. 이러한 상황은 다음과 같이 발생할 수 있습니다.

* `catalog::TimeStamp`, `vignette::TimeStamp` 또는 `attribute::TimeStamp`가 정의되지 않았으므로 [!DNL catalog.ini] 파일의 수정 시간이 `catalog::TimeStamp`의 기본값으로 사용됩니다.

* 네트워크 마운트를 통해 재료 카탈로그 파일을 공유하는 대신 각 서버에는 로컬 파일 시스템에 카탈로그 파일의 자체 인스턴스가 있습니다.
* 동일한 [!DNL catalog.ini] 파일의 두 개 이상의 인스턴스에 다른 파일 수정 날짜가 있으며, 파일 복사가 잘못되었을 수 있습니다.

## 속성 {#section-453952244193452caccfaf7f601007c1}

플래그. 비활성화하려면 0, 마지막으로 수정한 HTTP 헤더를 활성화하려면 1.

## 기본값 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

정의되지 않았거나 비어 있는 경우 `default::UseLastModified`에서 상속됩니다.

## 참조 {#section-1536715169da48b0aecc4ab7326c86db}

[카탈로그::타임스탬프](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [비네팅::타임스탬프](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
