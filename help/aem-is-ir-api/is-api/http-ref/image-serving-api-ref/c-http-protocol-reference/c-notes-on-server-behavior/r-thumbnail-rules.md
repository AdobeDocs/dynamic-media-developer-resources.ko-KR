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

1. If `catalog::ThumbType=Crop`그런 다음 (잘린) 이미지는 전체 대상 rect를 유지하면서 가능한 가장 작은 크기로 크기가 조정됩니다. If `catalog::ThumbType=Fit`그런 다음 (잘린) 이미지는 전체 이미지를 대상 rect에 맞추면서 가능한 가장 큰 크기로 크기가 조정됩니다. If `catalog::ThumbType=Texture`, (자른) 이미지는 다음 비율로 조정됩니다. `catalog::ThumbRes` 끝 `catalog::Resolution`.
1. 다음을 기준으로 대상 rect에 맞게 배율 조정된 이미지 정렬 `attribute::ThumbHorizAlign` 및 `attribute::ThumbVertAlign`.
1. 결과를 대상 rect로 자릅니다.
