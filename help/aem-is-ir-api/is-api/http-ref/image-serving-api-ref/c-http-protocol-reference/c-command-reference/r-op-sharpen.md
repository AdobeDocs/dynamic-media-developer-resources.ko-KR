---
description: 이미지를 선명하게 합니다. 레이어=comp인 경우 모든 비율 조정 후 레이어 또는 최종 보기 이미지에 기본 선명하게 하기 필터를 적용합니다.
seo-description: 이미지를 선명하게 합니다. 레이어=comp인 경우 모든 비율 조정 후 레이어 또는 최종 보기 이미지에 기본 선명하게 하기 필터를 적용합니다.
seo-title: op_sharpen
solution: Experience Manager
title: op_sharpen
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a00c60a-0d5c-4a99-a649-f29ebd710cf3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_sharpen{#op-sharpen}

이미지를 선명하게 합니다. 레이어=comp인 경우 모든 비율 조정 후 레이어 또는 최종 보기 이미지에 기본 선명하게 하기 필터를 적용합니다.

`op_sharpen=0|1`

레이어 마스크 또는 합성 마스크도 선명하게 됩니다.

## 속성 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

레이어 특성 또는 보기 속성입니다. 현재 레이어 또는 최종 보기 이미지에 적용됩니다( `layer=comp`경우). 효과 레이어에서 무시됩니다.

## 기본값 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`을 클릭하여 선명하게 하기 효과를 적용하지 않습니다.

## 예 {#section-3202122df5db4e14b358ecabfb6d8b85}

이미지 리샘플링으로 인해 발생하는 약간의 흐림 효과를 보정합니다. 또한 선명해진 가장자리를 따라 JPEG 결함이 추가로 발생하지 않도록 JPEG 품질을 높입니다.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 참조 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
