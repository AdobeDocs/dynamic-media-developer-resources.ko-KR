---
description: 이미지 크기 제한에 회신합니다. 클라이언트에 반환될 수 있는 최대 응답 이미지 폭과 높이입니다.
seo-description: 이미지 크기 제한에 회신합니다. 클라이언트에 반환될 수 있는 최대 응답 이미지 폭과 높이입니다.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# MaxPix{#maxpix}

이미지 크기 제한에 회신합니다. 클라이언트에 반환될 수 있는 최대 응답 이미지 폭과 높이입니다.

요청으로 인해 폭 또는 높이가 `attribute::MaxPix`보다 큰 응답 이미지가 표시되는 경우 서버에서 오류를 반환합니다.

## 속성 {#section-b175425b9e9f48e0b1a71640f6a9e936}

0보다 큰 정수 2개를 쉼표로 구분하여 입력합니다. 폭과 높이(픽셀 단위) 또한 `0,0`으로 설정하여 제한 없이 회신 이미지 크기를 허용할 수도 있습니다.

## 기본값 {#section-1003537434da432fb2af100ecdbf9d72}

정의되지 않았거나 비어 있는 경우 `default::MaxPix`에서 상속됩니다.

## 참조 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
