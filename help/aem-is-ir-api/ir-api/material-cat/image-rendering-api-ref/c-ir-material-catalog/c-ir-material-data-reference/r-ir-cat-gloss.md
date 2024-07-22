---
description: 서피스 광택 재료 서피스의 상대적 광택을 지정합니다.
solution: Experience Manager
title: 광택
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# 광택{#gloss}

서피스 광택 재료 서피스의 상대적 광택을 지정합니다.

이 값은 렌더러에서 다음 용도로 사용됩니다.

* `catalog::Illum`이(가) -1일 때 조명 맵을 선택합니다.
* `catalog::Type`과(와) 함께 광택 효과(정반사) 렌더링을 제어합니다.
* `catalog::Type` 및 `catalog::Roughness`과(와) 함께 3D 반사 렌더링 효과를 제어합니다.

## 속성 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

정수. 0...100 범위의 백분율 번호입니다. 모든 자재에 선택 사항입니다. 여러 반사 맵이 있는 비네팅 또는 3D 반사 기능이 있는 비네팅에만 사용됩니다. 알 수 없거나 필요하지 않은 경우 비워 두거나 -1로 설정합니다.

## 기본값 {#section-2352721073524f1a8d461f64a363aac9}

이 값을 -1로 설정하면 비네팅에서 기본값을 제공합니다.

## 참조 {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
