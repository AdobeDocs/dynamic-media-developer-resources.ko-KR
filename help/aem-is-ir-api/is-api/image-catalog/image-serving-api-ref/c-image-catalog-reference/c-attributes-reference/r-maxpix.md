---
description: 회신 이미지 크기 제한. 클라이언트에 반환될 수 있는 최대 응답 이미지 너비와 높이입니다.
seo-description: 회신 이미지 크기 제한. 클라이언트에 반환될 수 있는 최대 응답 이미지 너비와 높이입니다.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MaxPix{#maxpix}

회신 이미지 크기 제한. 클라이언트에 반환될 수 있는 최대 응답 이미지 너비와 높이입니다.

요청 시 너비 또는 높이가 `attribute::MaxPix`보다 큰 응답 이미지가 발생할 경우 서버가 오류를 반환합니다.

## 속성 {#section-b175425b9e9f48e0b1a71640f6a9e936}

0보다 큰 정수 두 개를 쉼표로 구분하여 지정합니다. 너비 및 높이(픽셀 단위) 또한 제한 없이 회신 이미지 크기를 허용하도록 `0,0` 설정할 수 있습니다.

## 기본값 {#section-1003537434da432fb2af100ecdbf9d72}

정의되지 않았거나 비어 있는 `default::MaxPix` 경우 상속됩니다.

## 참조 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
