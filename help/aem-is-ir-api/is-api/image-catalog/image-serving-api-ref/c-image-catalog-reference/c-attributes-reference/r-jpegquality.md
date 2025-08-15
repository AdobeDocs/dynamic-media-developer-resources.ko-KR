---
description: 기본 JPEG 인코딩 속성입니다. JPEG 응답 이미지의 기본 특성을 지정합니다.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# JpegQuality{#jpegquality}

기본 JPEG 인코딩 속성입니다. JPEG 응답 이미지의 기본 특성을 지정합니다.

## 속성 {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

쉼표로 구분된 정수 및 플래그. 첫 번째 값은 1..100 범위에 있으며 품질을 정의합니다. 제2 값은 정상 동작에 대해 0일 수 있고, 또는 JPEG 인코더들에 의해 보통 채용되는 RGB 색도 다운샘플링을 비활성화하기 위해 1일 수 있다.

## 기본값 {#section-0b25eddd59bc434abfe38eeea9d45df3}

정의되지 않았거나 비어 있는 경우 `default::JpegQuality`에서 상속됩니다.

## 참조 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
