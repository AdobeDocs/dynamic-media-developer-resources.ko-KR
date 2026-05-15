---
title: 리소스 모드
description: 기본 재샘플링 모드. 이미지 데이터 크기를 조정하는 데 사용할 기본 재샘플링 및 보간 특성을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
TQID: 'https://experienceleague.adobe.com/jYteRal6Z6ea7AWTuoGA9KFDAyPS1rV7t-KzZBbm-s0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 3%

---

# 리소스 모드{#resmode}

기본 재샘플링 모드. 이미지 데이터 크기를 조정하는 데 사용할 기본 재샘플링 및 보간 특성을 지정합니다.

요청에 `resMode=`이(가) 지정되지 않은 경우 사용됩니다.

## 속성 {#section-493f900be522486f97710cebdc4460c2}

열거형. `bilin`의 경우 2, `bicub`의 경우 3 또는 `sharp2` 보간 모드의 경우 4로 설정합니다(자세한 내용은 [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) 참조). `sharp` (1)은(는) 더 이상 사용되지 않습니다. 최상의 결과를 얻으려면 대신 `sharp2`(4)를 사용하십시오.

## 기본값 {#section-35f980e745fc4d79a2621e8abacc724d}

정의되지 않았거나 비어 있는 경우 `default::ResMode`에서 상속됩니다.

## 참조 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
