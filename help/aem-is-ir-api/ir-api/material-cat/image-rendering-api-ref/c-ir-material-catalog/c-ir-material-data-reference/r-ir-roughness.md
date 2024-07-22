---
description: 표면 거칠기. 재료 서피스의 상대적 광택을 지정합니다. 카탈로그 유형 및 카탈로그 광택과 함께 사용하여 3D 반사 렌더링 효과를 제어합니다.
solution: Experience Manager
title: 거칠음
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# 거칠음{#roughness}

표면 거칠기. 재료 서피스의 상대적 광택을 지정합니다. 3D 반사 렌더링 효과를 제어하기 위해 catalog::Type 및 catalog::Gloss와 함께 사용됩니다.

## 속성 {#section-70c3f2394fd8477ca83a369448907971}

정수. 0...100 범위의 백분율 값입니다. 모든 자재에 선택 사항입니다. 여러 반사 맵이 있는 비네팅 또는 3D 반사 기능이 있는 비네팅에만 사용됩니다. 알 수 없거나 필요하지 않은 경우 비워 두거나 -1로 설정합니다.

## 기본값 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1. 서버 기본값이 사용됩니다.

## 참조 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[황삭=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [카탈로그::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [카탈로그::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
