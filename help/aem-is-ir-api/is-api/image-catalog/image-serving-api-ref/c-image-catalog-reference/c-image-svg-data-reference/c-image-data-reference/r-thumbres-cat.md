---
description: 썸네일 해상도. 축소판 이미지의 개체 해상도를 지정합니다.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '70'
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

[catalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [attribute::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [썸네일 크기 조정](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
