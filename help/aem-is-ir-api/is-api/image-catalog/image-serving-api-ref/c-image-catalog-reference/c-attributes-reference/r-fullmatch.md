---
description: 카탈로그 일치 옵션.
seo-description: 카탈로그 일치 옵션.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---


# FullMatch{#fullmatch}

카탈로그 일치 옵션.

카탈로그 항목은 HTTP 요청에서 `*`rootId`*/ *`imageId`*` 쌍으로 지정됩니다. 구문 분석 시 `*`rootId`*`가 카탈로그의 `attribute::RootId` 값과 일치하고 카탈로그 레코드는 `*`imageId`*`와 `catalog::Id` 값을 일치시켜 식별됩니다. 카탈로그가 있지만 `*`imageId`*`와 일치하는 카탈로그 항목이 없는 경우 서버는 다음 두 가지 작업 중 하나를 수행할 수 있습니다.

`attribute::FullMatch`이(가) 설정되어 있지 않으면 서버는 일치하는 카탈로그의 특성을 사용합니다. 이 경우 `*`rootId`*`는 `attribute::RootPath`(또는 이 카탈로그에 지정되지 않은 경우 `default::RootPath`)으로 대체됩니다.

`attribute::FullMatch`이(가) 설정된 경우 서버는 카탈로그가 일치되지 않은 것처럼 카탈로그를 완전히 무시하고 기본 카탈로그 특성을 계속 사용합니다. 이 경우 `*`rootId`*`는 경로의 일부(이 경로는 `default::RootPath`에 의해 접두사로 표시됨)로 남습니다.

## 속성 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

플래그. 기본 비헤이비어는 0으로, 전체 일치 비헤이비어는 1로 설정합니다.

## 기본값 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

정의되지 않았거나 비어 있는 경우 `default::FullMatch`에서 상속됩니다.

## 참조 {#section-42da0ba53e0b4c089c62108785faf5a9}

[속성::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [카탈로그::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
