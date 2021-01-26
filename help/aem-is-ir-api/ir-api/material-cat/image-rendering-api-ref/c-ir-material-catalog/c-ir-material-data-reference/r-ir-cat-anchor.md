---
description: 이미지 앵커. 반복 가능한 텍스처, 벽 테두리 또는 디컬한 이미지의 기준점(핫스팟)을 지정합니다.
seo-description: 이미지 앵커. 반복 가능한 텍스처, 벽 테두리 또는 디컬한 이미지의 기준점(핫스팟)을 지정합니다.
seo-title: 앵커
solution: Experience Manager
title: 앵커
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---


# 앵커{#anchor}

이미지 앵커. 반복 가능한 텍스처, 벽 테두리 또는 디컬한 이미지의 기준점(핫스팟)을 지정합니다.

반복 가능한 텍스처는 텍스처 기준점이 개체의 텍스처 원점에 있도록 비네팅 개체에 적용됩니다. 비네팅 오브젝트에 디컬한 이미지가 적용되므로 디컬한 기준점이 오브젝트의 디테일 원점에 위치합니다. 벽 테두리의 경우 x 값만 사용됩니다.y 값은 무시됩니다.

## 속성 {#section-bc4bc8b897c64535b88681e57d72942f}

2개의 정수(쉼표로 구분) 이미지의 왼쪽 위 모서리를 기준으로 한 픽셀 오프셋입니다. `catalog::Alignment=3` 및 단색 및 캐비닛 재질이 있는 경우 무시됩니다.

## 기본값 {#section-b7ccc419a356415294706cd295ae96c9}

필드가 비어 있거나 없는 경우 반복 가능한 텍스처 재질에 대한 이미지의 왼쪽 위 모서리(0,0)가 사용되거나 디컬한 재질의 경우 이미지의 중심이 사용됩니다.

## 참조 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[카탈로그::정렬](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [앵커=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
