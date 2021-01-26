---
description: 기본 보기 크기입니다.
seo-description: 기본 보기 크기입니다.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 4%

---


# DefaultPix{#defaultpix}

기본 보기 크기입니다.

요청이 `wid=`, `hei=` 또는 `scl=`를 사용하여 명시적으로 보기 크기를 지정하지 않을 경우 서버는 응답 이미지를 이 폭 및 높이보다 작게 제한합니다.

## 속성 {#section-c3e658cf82c540d986b118f74f0fe1b2}

0 이상의 정수를 쉼표로 구분하여 2개의 정수입니다. 폭과 높이(픽셀 단위) 두 값 중 하나 또는 둘 모두를 0으로 설정하여 제한되지 않도록 할 수 있습니다.

중첩/포함된 요청에 적용되지 않습니다.

## 기본값 {#section-b7338b2bf5114fff83b0714a57b20639}

정의되지 않았거나 비어 있는 경우 `default::DefaultPix`에서 상속됩니다.

## 참조 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [카탈로그::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
