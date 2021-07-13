---
description: 재샘플링 모드. resMode= 기본값은 입니다. 렌더링된 이미지를 최종 크기로 조정하는 데 사용되는 리샘플링 및 보간 속성을 지정합니다.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c57932a0-529c-4f31-b60e-a38de6fe277f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---

# ResMode{#resmode}

재샘플링 모드. resMode= 기본값은 입니다. 렌더링된 이미지를 최종 크기로 조정하는 데 사용되는 리샘플링 및 보간 속성을 지정합니다.

## 속성 {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

열거형. `'bilin'`, `'bicub'` 의 경우 3, `'sharp2'` 보간 모드의 경우 4로 설정합니다(자세한 내용은 ` [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)` 참조).

## 기본값 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

정의되지 않았거나 비어 있는 경우 `default::ResMode`에서 상속됩니다.

## 참조 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
