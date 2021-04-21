---
description: 상대 이미지 URL에 대한 루트 URL. 상대 이미지 URL에 대한 루트 URL을 지정합니다.
solution: Experience Manager
title: 루트 URL
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# RootUrl{#rooturl}

상대 이미지 URL에 대한 루트 URL. 상대 이미지 URL에 대한 루트 URL을 지정합니다.

`attribute::RootUrl` 또는 값을 { `attribute::RootPath` 중괄호}  `src=` 또는  `mask=` (괄호)로 묶을 때 대신 사용됩니다.

## 속성 {#section-fe02269b4b724319a5d1f2cfcae31cba}

텍스트 문자열 값입니다. 선도적인 프로토콜 식별자를 포함한 절대 URL 루트 경로입니다. 다음 프로토콜이 지원됩니다.HTTP, HTTPS 및 FTP를 참조하십시오.

## 기본값 {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

정의되지 않은 경우 `default::RootUrl`에서 상속됩니다. 정의되었지만 비어 있는 경우, 상대 URL은 이 이미지 카탈로그에서 지원되지 않습니다.

## 참조 {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [속성:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [규칙 세트::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
