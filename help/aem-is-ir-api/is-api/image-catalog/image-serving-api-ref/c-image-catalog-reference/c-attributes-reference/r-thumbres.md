---
description: 기본 축소판 해상도입니다. 특정 카탈로그 레코드에 유효한 카탈로그 ThumbRes 값이 없는 경우 축소판 개체 해상도의 기본값을 제공합니다.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# ThumbRes{#thumbres}

기본 축소판 해상도입니다. 특정 카탈로그 레코드에 유효한 카탈로그::ThumbRes 값이 없는 경우 축소판 개체 해상도의 기본값을 제공합니다.

축소판 요청( `req=tmb`)과 `catalog::ThumbType=3`인 경우에만 사용됩니다.

## 속성 {#section-88d37d0e030f4879a9e584dd2cc780f3}

실제 숫자(0.보다 큼)는 일반적으로 인치당 픽셀로 표시되지만 미터당 픽셀과 같은 다른 단위로 표시될 수도 있습니다.

## 기본값 {#section-86588899ec9b4276a98b03d7faf64003}

정의되지 않았거나 비어 있는 경우 `default::ThumbRes`에서 상속됩니다.

## 참조 {#section-a6d2cce2e404441a996dba98a95c8e16}

[카탈로그::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
