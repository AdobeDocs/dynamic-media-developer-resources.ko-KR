---
description: 이러한 축소판 규칙에 주의하십시오.
solution: Experience Manager
title: 축소판 규칙
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 축소판 규칙{#thumbnail-rules}

이러한 축소판 규칙에 주의하십시오.

1. `catalog::ThumbType=Crop`이면 전체 대상 레코드를 덮어쓰는 동안 (잘린) 이미지가 가능한 가장 작은 크기로 조정됩니다. `catalog::ThumbType=Fit`이면 (잘린) 이미지는 최대 크기로 조정되지만 여전히 전체 이미지를 대상 레코드에 맞춥니다. `catalog::ThumbType=Texture`이면 (잘린) 이미지가 `catalog::ThumbRes` 대 `catalog::Resolution`의 비율로 조정됩니다.
1. `attribute::ThumbHorizAlign` 및 `attribute::ThumbVertAlign`을(를) 기준으로 크기가 조정된 이미지를 대상 레코드와 맞춥니다.
1. 결과를 타겟 레코드까지 자릅니다.
