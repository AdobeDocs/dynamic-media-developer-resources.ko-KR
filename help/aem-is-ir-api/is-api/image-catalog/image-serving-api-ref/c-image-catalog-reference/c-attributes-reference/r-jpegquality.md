---
description: 기본 JPEG 인코딩 속성입니다. JPEG 응답 이미지의 기본 특성을 지정합니다.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
TQID: 'https://experienceleague.adobe.com/eiTYLhEUblxZFnJJf5cWgrHF4qglIYB72m-COXeGc5A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
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
