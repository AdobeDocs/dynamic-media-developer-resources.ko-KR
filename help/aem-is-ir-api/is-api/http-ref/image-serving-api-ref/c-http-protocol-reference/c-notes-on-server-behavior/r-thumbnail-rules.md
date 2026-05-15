---
description: 이러한 썸네일 규칙을 알고 있어야 합니다.
solution: Experience Manager
title: 썸네일 규칙
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# 썸네일 규칙{#thumbnail-rules}

이러한 썸네일 규칙을 알고 있어야 합니다.

1. `catalog::ThumbType=Crop`이면 (잘린) 이미지는 전체 대상 rect를 유지하면서 가능한 가장 작은 크기로 크기가 조정됩니다. `catalog::ThumbType=Fit`이면 (잘린) 이미지는 전체 이미지를 대상 rect에 맞추는 동안 가능한 가장 큰 크기로 크기가 조정됩니다. `catalog::ThumbType=Texture`이면 (잘린) 이미지는 `catalog::ThumbRes`과(와) `catalog::Resolution`의 비율로 조정됩니다.
1. `attribute::ThumbHorizAlign` 및 `attribute::ThumbVertAlign`을(를) 기준으로 대상 rect에 맞춰 크기 조정된 이미지를 정렬합니다.
1. 결과를 대상 rect로 자릅니다.
