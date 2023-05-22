---
description: 썸네일에 대한 세로 정렬. wid= 및 hei= 또는 DefaultThumbPix 특성으로 지정된 응답 이미지 사각형에서 썸네일 이미지의 수직 정렬을 지정합니다.
solution: Experience Manager
title: ThumbVertAlign
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bb1aa398-5638-4109-bf05-bc51ace4146d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# ThumbVertAlign{#thumbvertalign}

썸네일에 대한 세로 정렬. wid= 및 hei= 또는 특성::DefaultThumbPix로 지정된 응답 이미지 사각형에서 썸네일 이미지의 수직 정렬을 지정합니다.

썸네일 요청에만 사용됩니다( `req=tmb`).

## 속성 {#section-f02c23248e87419caf3d95add51aea1e}

열거형. 위쪽, 가운데 및 아래쪽 정렬에 대해 허용되는 값은 각각 1, 2 및 3입니다.

## 기본값 {#section-30caa4e772254419ad7a3a89d440666c}

상속 위치 `default::ThumbHorizAlign` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[catalog::ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md) , [attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
