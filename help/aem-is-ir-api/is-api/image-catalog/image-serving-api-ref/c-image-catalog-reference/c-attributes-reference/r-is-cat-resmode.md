---
description: 기본 리샘플링 모드. 이미지 데이터 크기 조정에 사용할 기본 리샘플링 및 보간 속성을 지정합니다.
seo-description: 기본 리샘플링 모드. 이미지 데이터 크기 조정에 사용할 기본 리샘플링 및 보간 속성을 지정합니다.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ResMode{#resmode}

기본 리샘플링 모드. 이미지 데이터 크기 조정에 사용할 기본 리샘플링 및 보간 속성을 지정합니다.

요청에 지정되지 `resMode=` 않은 경우에 사용됩니다.

## 속성 {#section-493f900be522486f97710cebdc4460c2}

열거형. 보간 모드를 `bilin`위해 2, 3 `bicub`또는 4로 설정합니다(자세한 내용은 `sharp2` ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` 참조). `sharp` (1)는 더 이상 사용되지 않습니다. 최상의 결과를 얻으려면 `sharp2` (4)를 대신 사용하십시오.

## 기본값 {#section-35f980e745fc4d79a2621e8abacc724d}

정의되지 않았거나 비어 있는 `default::ResMode` 경우 상속됩니다.

## 참조 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
