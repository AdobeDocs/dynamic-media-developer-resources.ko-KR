---
description: 축소판의 세로 정렬. wid= 및 hei= 또는 DefaultThumbPix 속성으로 지정된 응답 이미지 사각형에 축소판 이미지의 세로 정렬을 지정합니다.
solution: Experience Manager
title: ThumbVertAlign
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: bb1aa398-5638-4109-bf05-bc51ace4146d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# ThumbVertAlign{#thumbvertalign}

축소판의 세로 정렬. wid= 및 hei= 또는 attribute::DefaultThumbPix로 지정된 응답 이미지 사각형에 축소판 이미지의 세로 정렬을 지정합니다.

축소판 요청( `req=tmb`)에만 사용됩니다.

## 속성 {#section-f02c23248e87419caf3d95add51aea1e}

열거형. 허용되는 값은 각각 위쪽, 가운데 및 아래쪽 정렬의 경우 1, 2 및 3입니다.

## 기본값 {#section-30caa4e772254419ad7a3a89d440666c}

정의되지 않았거나 비어 있는 경우 `default::ThumbHorizAlign`에서 상속됩니다.

## 참조 {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[catalog::ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md) ,  [attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
