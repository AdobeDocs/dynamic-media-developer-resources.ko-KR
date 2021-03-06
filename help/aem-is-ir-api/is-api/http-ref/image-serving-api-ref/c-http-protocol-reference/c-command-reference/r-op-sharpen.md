---
description: 이미지를 선명하게 합니다. 레이어=comp인 경우 모든 비율 조정 후 레이어 또는 최종 보기 이미지에 기본 선명도 필터를 적용합니다.
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# op_선명하게{#op-sharpen}

이미지를 선명하게 합니다. 레이어=comp인 경우 모든 비율 조정 후 레이어 또는 최종 보기 이미지에 기본 선명도 필터를 적용합니다.

`op_sharpen=0|1`

레이어 마스크나 복합 마스크도 선명하게 표시됩니다.

## 속성 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

레이어 특성 또는 보기 속성입니다. `layer=comp`인 경우 현재 레이어 또는 최종 보기 이미지에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`: 선명하게 하지 않음 효과입니다.

## 예 {#section-3202122df5db4e14b358ecabfb6d8b85}

이미지 재샘플링으로 인해 발생하는 약간 흐림 현상을 보정합니다. 또한 선명하게 된 가장자리를 따라 추가 JPEG 가공물이 발생하지 않도록 JPEG 품질을 높입니다.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 참조 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
