---
description: 이러한 축소판 규칙에 주의하십시오.
seo-description: 이러한 축소판 규칙에 주의하십시오.
seo-title: 축소판 규칙
solution: Experience Manager
title: 축소판 규칙
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# 축소판 규칙{#thumbnail-rules}

이러한 축소판 규칙에 주의하십시오.

1. `catalog::ThumbType=Crop`인 경우 전체 대상 사각형을 포함하는 동안 이미지 크기가 가능한 최소 크기로 조정됩니다. `catalog::ThumbType=Fit`인 경우(잘린) 이미지는 전체 이미지를 대상 대상에 맞추면서 가능한 가장 큰 크기로 조절됩니다. `catalog::ThumbType=Texture`인 경우(잘린) 이미지는 `catalog::ThumbRes` 대 `catalog::Resolution`의 비율로 조절됩니다.
1. 비율 조정된 이미지를 `attribute::ThumbHorizAlign` 및 `attribute::ThumbVertAlign`을 기준으로 대상 맞춥니다.
1. 결과를 대상 사각형으로 자릅니다.

