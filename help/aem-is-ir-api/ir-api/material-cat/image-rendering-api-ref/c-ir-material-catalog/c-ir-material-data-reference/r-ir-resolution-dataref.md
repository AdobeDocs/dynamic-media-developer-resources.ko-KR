---
description: 해결 방법. "실제" 이미지 해상도는 일반적으로 인치당 픽셀로 표시되지만, 미터당 픽셀과 같은 다른 단위일 수도 있습니다.
solution: Experience Manager
title: 해상도
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# 해상도{#resolution}

해결 방법. &quot;실제&quot; 이미지 해상도는 일반적으로 인치당 픽셀로 표시되지만, 미터당 픽셀과 같은 다른 단위일 수도 있습니다.

## 속성 {#section-985ca2ad858c4e9c9cbb303f55447553}

0보다 큰 실수. 이미지 해상도가 attribute::Resolution과 동일하지 않은 경우 텍스처 및 데칼 재료에 필요합니다. 단색 및 캐비닛 소재에서 무시됩니다.

## 기본값 {#section-b1d044e211194242a900aaef4a8c8e6f}

필드가 없거나 값이 0 또는 음수이거나 필드가 비어 있는 경우 `attribute::Resolution`이(가) 사용됩니다.

## 참조 {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
