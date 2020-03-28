---
description: 기본 보기 크기입니다.
seo-description: 기본 보기 크기입니다.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultPix{#defaultpix}

기본 보기 크기입니다.

The server constrains reply images to be no larger than this width and height, if the request does not specify the view size explicitly using `wid=`, `hei=`, or `scl=`.

## 속성 {#section-c3e658cf82c540d986b118f74f0fe1b2}

0보다 큰 정수 2개를 쉼표로 구분하여 지정합니다. 너비 및 높이(픽셀 단위) 두 값 중 하나 또는 둘 다 0으로 설정하여 제한을 해제할 수 있습니다.

중첩/임베디드 요청에는 적용되지 않습니다.

## 기본값 {#section-b7338b2bf5114fff83b0714a57b20639}

정의되지 않았거나 비어 있는 `default::DefaultPix` 경우 상속됩니다.

## 참조 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
