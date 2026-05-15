---
description: 썸네일 해상도. 축소판 이미지의 개체 해상도를 지정합니다.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
TQID: 'https://experienceleague.adobe.com/A7vuk3uRPTC-EUgmh4OhVHYYA4BThHxD0vMnB3yw1Bs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 69
ht-degree: 4%

---

# ThumbRes{#thumbres}

썸네일 해상도. 축소판 이미지의 개체 해상도를 지정합니다.

`catalog::ThumbType=3`인 경우에만 사용됩니다.

## 속성 {#section-ee5cae086a3d4875805fa8a08756a586}

실수 값이 0보다 큼. `catalog::Resolution`과(와) 같은 단위를 사용해야 합니다.

## 기본값 {#section-f0e453fc8a7c451db21961c084eecabd}

필드가 없거나 값이 0이거나 필드가 비어 있는 경우 `attribute::ThumbRes`이(가) 사용됩니다.

## 참조 {#section-eb716bf647614db083020fe8ce453751}

[카탈로그:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , [카탈로그::해상도](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [특성::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [썸네일 크기 조정](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
