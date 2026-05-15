---
description: 상대 이미지 URL의 루트 URL입니다. 상대 이미지 URL의 루트 URL을 지정합니다.
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
TQID: 'https://experienceleague.adobe.com/c-jvMp3XvBjonacYBfmA7b8MnA83SKi2lsO9YJLPqis'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 3%

---

# RootUrl{#rooturl}

상대 이미지 URL의 루트 URL입니다. 상대 이미지 URL의 루트 URL을 지정합니다.

`src=` 또는 `mask=` 값이 {curly braces} 또는 (괄호)로 둘러싸인 경우 `attribute::RootPath` 대신 `attribute::RootUrl`이(가) 사용됩니다.

## 속성 {#section-fe02269b4b724319a5d1f2cfcae31cba}

텍스트 문자열 값입니다. 선행 프로토콜 식별자를 포함하는 절대 URL 루트 경로입니다. 지원되는 프로토콜은 HTTP, HTTPS 및 FTP입니다.

## 기본값 {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

정의되지 않은 경우 `default::RootUrl`에서 상속됩니다. 정의되어 있지만 비어 있는 경우 상대 URL은 이 이미지 카탈로그에서 지원되지 않습니다.

## 참조 {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [규칙 집합::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
