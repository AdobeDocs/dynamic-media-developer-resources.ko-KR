---
description: 표면 광택 재료 서피스의 상대 광택 효과를 지정합니다.
seo-description: 표면 광택 재료 서피스의 상대 광택 효과를 지정합니다.
seo-title: 광택 효과
solution: Experience Manager
title: 광택 효과
topic: Scene7 Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---


# 광택{#gloss}

표면 광택 재료 서피스의 상대 광택 효과를 지정합니다.

이 값은 렌더러에서 다음 용도로 사용됩니다.

* `catalog::Illum`이(가) -1이면 조명 맵을 선택합니다.
* `catalog::Type`과 함께 광택 효과(반사광) 렌더링을 제어합니다.
* `catalog::Type` 및 `catalog::Roughness`과 함께 3D 반사 렌더링 효과를 제어합니다.

## 속성 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

정수 번호입니다. 0...100 범위의 백분율 번호입니다. 모든 자료에 선택 사항. 여러 개의 반사 맵 또는 3D 반사 기능이 있는 비네팅을 사용하는 비네팅에만 사용됩니다. 알려지거나 필요하지 않은 경우 비워 두거나 -1로 설정합니다.

## 기본값 {#section-2352721073524f1a8d461f64a363aac9}

이 값이 -1로 설정된 경우 비네팅에서 기본값을 제공합니다.

## 참조 {#section-0213bbdb7d6d4974a7c53822957717c1}

[glossing=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [카탈로그::거칠음](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99),  [카탈로그::유형](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
