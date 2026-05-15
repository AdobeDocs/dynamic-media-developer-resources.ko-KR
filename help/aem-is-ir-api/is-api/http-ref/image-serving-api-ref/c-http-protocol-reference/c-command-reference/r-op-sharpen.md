---
title: op_sharpen
description: 이미지를 선명하게 합니다. 레이어=comp인 경우 모든 크기 조정 후에 기본 선명하게 하기 필터를 레이어나 최종 뷰 이미지에 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
TQID: 'https://experienceleague.adobe.com/CLyNZKJir4mYZ2L04ZKpnkNk6LX9xs8VUwnwwPrs-Zc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 3%

---

# op_sharpen{#op-sharpen}

이미지를 선명하게 합니다. 레이어=comp인 경우 모든 크기 조정 후에 기본 선명하게 하기 필터를 레이어나 최종 뷰 이미지에 적용합니다.

`op_sharpen=0|1`

레이어 마스크 또는 복합 마스크도 선명하게 됩니다.

## 속성 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Layer 속성 또는 view 속성. `layer=comp`인 경우 현재 레이어 또는 최종 보기 이미지에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`(선명하게 하기 효과 없음).

## 예 {#section-3202122df5db4e14b358ecabfb6d8b85}

이미지 리샘플링으로 인해 약간 흐려지는 점을 보완합니다. 또한 선명해진 가장자리를 따라 추가 JPEG 아티팩트가 생기지 않도록 JPEG 품질을 높입니다.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 참조 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
