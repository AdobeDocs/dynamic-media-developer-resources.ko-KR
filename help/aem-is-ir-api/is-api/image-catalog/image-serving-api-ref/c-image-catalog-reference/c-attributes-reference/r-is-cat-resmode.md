---
title: ResMode
description: 기본 재샘플링 모드입니다. 이미지 데이터 크기 조절에 사용할 기본 리샘플링 및 보간 속성을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# ResMode{#resmode}

기본 재샘플링 모드입니다. 이미지 데이터 크기 조절에 사용할 기본 리샘플링 및 보간 속성을 지정합니다.

다음 경우에 사용됩니다. `resMode=` 이 요청에 지정되지 않았습니다.

## 속성 {#section-493f900be522486f97710cebdc4460c2}

열거형. 에 대해 2로 설정 `bilin`, 3에 대해 `bicub`, 4에 대해 `sharp2` 보간 모드(참조) [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) 자세한 내용). `sharp` (1)은 더 이상 사용되지 않습니다. 사용 `sharp2` (4) 대신 사용할 수 있습니다.

## 기본값 {#section-35f980e745fc4d79a2621e8abacc724d}

상속됨 `default::ResMode` 정의되지 않았거나 비어 있는 경우.

## 참조 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
