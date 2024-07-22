---
description: 이미지 앵커. 반복 가능한 텍스처, 벽 테두리 또는 전사 이미지의 기준점(핫스팟)을 지정합니다.
solution: Experience Manager
title: 앵커
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# 앵커{#anchor}

이미지 앵커. 반복 가능한 텍스처, 벽 테두리 또는 전사 이미지의 기준점(핫스팟)을 지정합니다.

반복 가능한 텍스처는 텍스처 기준점이 오브젝트의 텍스처 원점에 위치하도록 비네팅 오브젝트에 적용됩니다. 데칼 이미지는 비네팅 오브젝트에 적용되어 데칼 기준점이 오브젝트의 데칼 원점에 위치합니다. 벽 경계의 경우 x 값만 사용되고 y 값은 무시됩니다.

## 속성 {#section-bc4bc8b897c64535b88681e57d72942f}

쉼표로 구분된 2개의 정수. 이미지의 위쪽, 왼쪽 모서리를 기준으로 한 픽셀 오프셋입니다. `catalog::Alignment=3`인 경우 및 단색 및 캐비닛 자재별로 무시됩니다.

## 기본값 {#section-b7ccc419a356415294706cd295ae96c9}

필드가 비어 있거나 없으면 반복 가능한 질감 재료에 대한 이미지의 왼쪽 상단 모서리(0,0)를 사용하거나 데칼 재료인 경우 이미지의 중심을 사용합니다.

## 참조 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[카탈로그::정렬](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [앵커=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
