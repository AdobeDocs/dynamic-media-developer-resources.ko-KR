---
description: 기본 재샘플링 모드입니다. 이미지 데이터 크기 조절에 사용할 기본 리샘플링 및 보간 속성을 지정합니다.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ResMode{#resmode}

기본 재샘플링 모드입니다. 이미지 데이터 크기 조절에 사용할 기본 리샘플링 및 보간 속성을 지정합니다.

요청에 `resMode=`이 지정되지 않은 경우 사용됩니다.

## 속성 {#section-493f900be522486f97710cebdc4460c2}

열거형. `bilin`, `bicub` 의 경우 3, `sharp2` 보간 모드의 경우 4로 설정합니다(자세한 내용은 ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` 참조). `sharp` (1)은 더 이상 사용되지 않습니다. 최상의 결과를 얻으려면 `sharp2` (4)를 사용하십시오.

## 기본값 {#section-35f980e745fc4d79a2621e8abacc724d}

정의되지 않았거나 비어 있는 경우 `default::ResMode`에서 상속됩니다.

## 참조 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
