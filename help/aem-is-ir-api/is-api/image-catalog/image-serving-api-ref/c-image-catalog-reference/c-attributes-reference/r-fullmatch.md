---
description: 카탈로그 일치 옵션.
seo-description: 카탈로그 일치 옵션.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# FullMatch{#fullmatch}

카탈로그 일치 옵션.

카탈로그 항목은 HTTP 요청에서 ` *``*/ *`rootIdimageId`*` 쌍으로 지정됩니다. 구문 분석 시 ` *`rootId가`*` 카탈로그 `attribute::RootId` 값과 일치하는 경우 카탈로그가 선택되며, 카탈로그 레코드는 ` *`값과`*` imageId `catalog::Id` 를 일치시켜식별됩니다. 카탈로그가 있지만 imageId와 일치하는 카탈로그 항목이 ` *`없는`*`경우 서버는 다음 중 하나를 수행할 수 있습니다.

이 `attribute::FullMatch` 옵션이 설정되지 않으면 서버는 일치하는 카탈로그의 특성을 사용합니다. 이 경우 rootId ` *`는`*` (또는 이 카탈로그에 지정되지 않은 `attribute::RootPath` `default::RootPath`경우)로 대체됩니다.

이 `attribute::FullMatch` 옵션을 설정하면 카탈로그가 일치하지 않는 것처럼 서버가 카탈로그를 완전히 무시하고 기본 카탈로그 특성을 계속 사용합니다. 이 경우 rootId ` *`는`*` 경로의 일부로 남으며, 이 경로는 다음에 의해 접두사가 `default::RootPath`됩니다.

## 속성 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

플래그. 기본 비헤이비어는 0으로, 전체 일치 동작을 활성화하려면 1로 설정합니다.

## 기본값 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

정의되지 않았거나 비어 있는 `default::FullMatch` 경우 상속됩니다.

## 참조 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
