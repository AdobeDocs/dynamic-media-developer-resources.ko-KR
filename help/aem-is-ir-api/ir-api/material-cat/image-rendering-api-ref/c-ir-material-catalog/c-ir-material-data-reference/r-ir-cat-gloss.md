---
description: 표면 용어집 재료 서피스의 상대적 광택을 지정합니다.
seo-description: 표면 용어집 재료 서피스의 상대적 광택을 지정합니다.
seo-title: 광택
solution: Experience Manager
title: 광택
topic: Scene7 Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 광택{#gloss}

표면 용어집 재료 서피스의 상대적 광택을 지정합니다.

이 값은 렌더러에서 다음 용도로 사용됩니다.

* -1일 때 조명 맵을 `catalog::Illum` 선택합니다.
* 광택 효과(반사 반사) 렌더링을 함께 `catalog::Type`제어합니다.
* 및 과 함께 3D 반사 렌더링 효과를 `catalog::Type` 제어합니다 `catalog::Roughness`.

## 속성 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

정수 번호입니다. 0...100 범위의 백분율 번호입니다. 모든 자료에 대한 옵션 여러 개의 반사 맵이나 3D 반사 기능이 있는 비네팅을 사용하는 비네팅에만 사용됩니다. 알 수 없거나 필요하지 않은 경우 비워 두거나 -1로 설정합니다.

## 기본값 {#section-2352721073524f1a8d461f64a363aac9}

이 값이 -1로 설정된 경우 비네팅을 통해 기본값이 제공됩니다.

## 참조 {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
