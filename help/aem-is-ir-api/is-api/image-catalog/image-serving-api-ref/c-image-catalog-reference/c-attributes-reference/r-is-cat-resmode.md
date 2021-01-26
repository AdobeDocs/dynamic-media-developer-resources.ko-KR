---
description: 기본 리샘플링 모드입니다. 이미지 데이터의 크기 조정에 사용할 기본 리샘플링 및 보간 특성을 지정합니다.
seo-description: 기본 리샘플링 모드입니다. 이미지 데이터의 크기 조정에 사용할 기본 리샘플링 및 보간 특성을 지정합니다.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 5%

---


# ResMode{#resmode}

기본 리샘플링 모드입니다. 이미지 데이터의 크기 조정에 사용할 기본 리샘플링 및 보간 특성을 지정합니다.

요청에 `resMode=`이(가) 지정되지 않은 경우에 사용됩니다.

## 속성 {#section-493f900be522486f97710cebdc4460c2}

열거형. `bilin`, `bicub`의 경우 3, `sharp2` 보간 모드의 경우 4로 설정합니다(자세한 내용은 ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` 참조). `sharp` (1) 사용 중지되었습니다. 최상의 결과를 얻으려면 `sharp2`(4)을 대신 사용하십시오.

## 기본값 {#section-35f980e745fc4d79a2621e8abacc724d}

정의되지 않았거나 비어 있는 경우 `default::ResMode`에서 상속됩니다.

## 참조 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
