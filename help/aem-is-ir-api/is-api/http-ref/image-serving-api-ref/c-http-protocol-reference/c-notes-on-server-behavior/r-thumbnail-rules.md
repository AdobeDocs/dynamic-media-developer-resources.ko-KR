---
description: 이러한 썸네일 규칙을 알고 있어야 합니다.
solution: Experience Manager
title: 썸네일 규칙
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# 썸네일 규칙{#thumbnail-rules}

이러한 썸네일 규칙을 알고 있어야 합니다.

1. `catalog::ThumbType=Crop`이면 (잘린) 이미지는 전체 대상 rect를 유지하면서 가능한 가장 작은 크기로 크기가 조정됩니다. `catalog::ThumbType=Fit`이면 (잘린) 이미지는 전체 이미지를 대상 rect에 맞추는 동안 가능한 가장 큰 크기로 크기가 조정됩니다. `catalog::ThumbType=Texture`이면 (잘린) 이미지는 `catalog::ThumbRes`과(와) `catalog::Resolution`의 비율로 조정됩니다.
1. `attribute::ThumbHorizAlign` 및 `attribute::ThumbVertAlign`을(를) 기준으로 대상 rect에 맞춰 크기 조정된 이미지를 정렬합니다.
1. 결과를 대상 rect로 자릅니다.
