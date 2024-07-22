---
title: JpegQuality
description: 기본 JPEG 인코딩 품질입니다. JPEG으로 인코딩된 응답 이미지의 기본 품질 설정을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# JpegQuality{#jpegquality}

기본 JPEG 인코딩 품질입니다. JPEG으로 인코딩된 응답 이미지의 기본 품질 설정을 지정합니다.

## 속성 {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

쉼표로 구분된 정수 및 플래그. 첫 번째 값은 1..100 범위에 있으며 품질을 정의합니다. 제2 값은 정상 동작에 대해 `0`일 수 있고, JPEG 인코더에 의해 채용된 색도 다운샘플링을 비활성화하기 위해 `1`일 수 있다.

## 기본값 {#section-60900c0fb8c54444b2361513232514db}

정의되지 않았거나 비어 있는 경우 `default::JpegQuality`에서 상속됩니다.

## 참조 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
