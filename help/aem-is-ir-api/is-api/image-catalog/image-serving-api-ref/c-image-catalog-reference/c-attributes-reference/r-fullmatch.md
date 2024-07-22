---
description: 카탈로그 일치 옵션.
solution: Experience Manager
title: 전체 일치
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# 전체 일치{#fullmatch}

카탈로그 일치 옵션.

카탈로그 항목이 HTTP 요청에서 `*`rootId`*/ *`imageId`*` 쌍으로 지정되었습니다. 구문 분석 시 `*`rootId`*`이(가) 카탈로그의 `attribute::RootId` 값과 일치하는 경우 카탈로그를 선택하고 `*`imageId`*`을(를) `catalog::Id` 값과 일치시켜 카탈로그 레코드를 식별합니다. 카탈로그를 찾았지만 `*`imageId`*`와(과) 일치하는 카탈로그 항목이 없는 경우 서버는 다음 두 가지 중 하나를 수행할 수 있습니다.

`attribute::FullMatch`이(가) 설정되지 않은 경우 서버는 일치하는 카탈로그의 특성을 사용합니다. 이 경우 `*`rootId`*`은(는) `attribute::RootPath`(또는 이 카탈로그에 지정되지 않은 경우 `default::RootPath`)로 대체됩니다.

`attribute::FullMatch`이(가) 설정되면 서버는 일치하는 카탈로그가 없는 것처럼 카탈로그를 완전히 무시하고 기본 카탈로그 특성을 사용하여 계속 진행합니다. 이 경우 `*`rootId`*`은(는) `default::RootPath` 앞에 추가된 경로의 일부로 유지됩니다.

## 속성 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

플래그. 기본 동작은 0으로 설정하고, 전체 일치 동작을 활성화하려면 1로 설정합니다.

## 기본값 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

정의되지 않았거나 비어 있는 경우 `default::FullMatch`에서 상속됩니다.

## 참조 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
