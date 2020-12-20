---
description: 축소판 해상도를 참조하십시오. 축소판 이미지의 개체 해상도를 지정합니다.
seo-description: 축소판 해상도를 참조하십시오. 축소판 이미지의 개체 해상도를 지정합니다.
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 10bbad31-a0fd-4ed3-b708-87822777acdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# ThumbRes{#thumbres}

축소판 해상도를 참조하십시오. 축소판 이미지의 개체 해상도를 지정합니다.

`catalog::ThumbType=3`인 경우에만 사용됩니다.

## 속성 {#section-ee5cae086a3d4875805fa8a08756a586}

0보다 큰 실수 값입니다. `catalog::Resolution`과(와) 동일한 단위를 가져야 합니다.

## 기본값 {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` 값이 0이거나 필드가 비어 있는 경우 필드가 없는 경우에 사용됩니다.

## 참조 {#section-eb716bf647614db083020fe8ce453751}

[카탈로그:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [카탈로그::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [속성::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)  [, 축소판 크기 조정](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
