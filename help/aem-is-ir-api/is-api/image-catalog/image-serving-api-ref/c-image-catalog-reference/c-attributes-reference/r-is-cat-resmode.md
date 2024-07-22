---
title: 리소스 모드
description: 기본 재샘플링 모드. 이미지 데이터 크기를 조정하는 데 사용할 기본 재샘플링 및 보간 특성을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# 리소스 모드{#resmode}

기본 재샘플링 모드. 이미지 데이터 크기를 조정하는 데 사용할 기본 재샘플링 및 보간 특성을 지정합니다.

요청에 `resMode=`이(가) 지정되지 않은 경우 사용됩니다.

## 속성 {#section-493f900be522486f97710cebdc4460c2}

열거형. `bilin`의 경우 2, `bicub`의 경우 3 또는 `sharp2` 보간 모드의 경우 4로 설정합니다(자세한 내용은 [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) 참조). `sharp`(1)은(는) 더 이상 사용되지 않습니다. 최상의 결과를 얻으려면 대신 `sharp2`(4)를 사용하십시오.

## 기본값 {#section-35f980e745fc4d79a2621e8abacc724d}

정의되지 않았거나 비어 있는 경우 `default::ResMode`에서 상속됩니다.

## 참조 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
