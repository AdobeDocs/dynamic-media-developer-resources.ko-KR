---
description: 해결 방법. "실제" 이미지 해상도는 일반적으로 인치당 픽셀로 표시되지만, 미터당 픽셀과 같은 다른 단위일 수도 있습니다.
solution: Experience Manager
title: 해상도
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
TQID: 'https://experienceleague.adobe.com/EV1kiy21nLXMKmrDDBQclvZvdB-h-zi9SCkskvzUJNQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 104
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

