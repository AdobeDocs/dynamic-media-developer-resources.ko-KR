---
description: 이미지 앵커. 반복 가능한 텍스쳐, 벽 테두리 또는 십진수 이미지의 기준점(핫스팟)을 지정합니다.
solution: Experience Manager
title: 앵커
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---

# 앵커{#anchor}

이미지 앵커. 반복 가능한 텍스쳐, 벽 테두리 또는 십진수 이미지의 기준점(핫스팟)을 지정합니다.

텍스처 기준점이 개체의 텍스처 원점에 위치하도록 비네팅 개체에 반복 가능한 텍스처가 적용됩니다. 비네팅 오브젝트에 비네팅 이미지가 적용되어 비네팅 기준점이 오브젝트의 비네팅 원점에 위치한다. 벽 테두리의 경우 x 값만 사용됩니다. y 값은 무시됩니다.

## 속성 {#section-bc4bc8b897c64535b88681e57d72942f}

쉼표로 구분된 두 정수 숫자. 이미지의 맨 위 왼쪽 모서리에 상대적인 픽셀 오프셋. `catalog::Alignment=3` 및 단색 및 캐비닛 재료에서 무시됩니다.

## 기본값 {#section-b7ccc419a356415294706cd295ae96c9}

필드가 비어 있거나 없는 경우 반복 가능한 텍스쳐 재질의 이미지의 왼쪽 위 모서리(0,0)가 사용되거나, 소수점 재질의 경우 이미지의 중심을 사용합니다.

## 참조 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[카탈로그::정렬](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [앵커=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
