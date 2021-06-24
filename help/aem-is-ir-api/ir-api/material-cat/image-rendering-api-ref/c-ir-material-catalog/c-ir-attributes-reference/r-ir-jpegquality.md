---
description: 기본 JPEG 인코딩 기능. JPEG로 인코딩된 회신 이미지에 대한 기본 품질 설정을 지정합니다.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# JpegQuality{#jpegquality}

기본 JPEG 인코딩 기능. JPEG로 인코딩된 회신 이미지에 대한 기본 품질 설정을 지정합니다.

## 속성 {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

쉼표로 구분된 정수 및 플래그. 첫 번째 값은 1.100 범위에 있고 품질을 정의합니다. 두 번째 값은 일반 동작의 경우 0이거나, 일반적으로 JPEG 인코더에 사용되는 색상 샘플링 다운샘플링을 비활성화하려면 1일 수 있습니다.

## 기본값 {#section-60900c0fb8c54444b2361513232514db}

정의되지 않았거나 비어 있는 경우 `default::JpegQuality`에서 상속됩니다.

## 참조 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
