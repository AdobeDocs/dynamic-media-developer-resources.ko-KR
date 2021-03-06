---
description: 카탈로그 식별자. HTTP 요청의 비네팅, 재료 또는 ICC 프로필 개체 지정자에서 이 카탈로그를 식별하는 데 사용할 HTTP 경로 요소입니다.
solution: Experience Manager
title: RootId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cc34087a-8a19-4ead-b510-f2466efc44a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# RootId{#rootid}

카탈로그 식별자. HTTP 요청의 비네팅, 재료 또는 ICC 프로필 개체 지정자에서 이 카탈로그를 식별하는 데 사용할 HTTP 경로 요소입니다.

## 속성 {#section-c33266223d5b47029df756caa4e0df0c}

텍스트 문자열 값입니다. http 경로에 유효한 모든 문자를 포함할 수 있습니다.

## 기본값 {#section-e0ed902557684345850b86672b5dbe5b}

없음. 각 카탈로그에는 고유한 `catalog::RootId` 값이 있어야 합니다. default.ini에는 일반적으로 빈 `catalog::RootId`이 있습니다.

## 참조 {#section-4670832574f54f9080bb485b047efd5b}

[catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85) ,  [vignette::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-id-vignette.md#reference-2a7ba758924b4757b3234942304db7fd),  [profile::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-macro-definition-reference/r-ir-name.md#reference-63b663d2052545ffab030a23e7060b1e),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
