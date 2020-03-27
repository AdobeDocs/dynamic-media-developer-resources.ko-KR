---
description: 이러한 축소판 규칙에 주의하십시오.
seo-description: 이러한 축소판 규칙에 주의하십시오.
seo-title: 축소판 규칙
solution: Experience Manager
title: 축소판 규칙
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 축소판 규칙{#thumbnail-rules}

이러한 축소판 규칙에 주의하십시오.

1. 이 `catalog::ThumbType=Crop`경우 (잘린) 이미지는 전체 대상 사각형을 포함하는 동안 가능한 가장 작은 크기로 조정됩니다. 이 `catalog::ThumbType=Fit`경우, (잘린) 이미지는 최대 크기로 조절되고 전체 이미지를 대상 대상에 맞게 조정할 수 있습니다. 이 `catalog::ThumbType=Texture`경우, (잘림) 이미지는 `catalog::ThumbRes` 비율 대 `catalog::Resolution`로 조정됩니다.
1. 및 을 기준으로 대상 사각형에 맞춰 비율 조정된 이미지를 `attribute::ThumbHorizAlign` 정렬합니다 `attribute::ThumbVertAlign`.
1. 결과를 대상 사각형으로 자릅니다.

