---
title: 리소스 모드
description: 재샘플링 모드. resMode=의 기본값 렌더링된 이미지의 크기를 최종 크기로 조정하는 데 사용되는 재샘플링 및 보간 특성을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c57932a0-529c-4f31-b60e-a38de6fe277f
TQID: 'https://experienceleague.adobe.com/FZ76OaQf5qTWEDjwaLQ38GcgXsSnemM8xST9CmH9HPs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# 리소스 모드{#resmode}

재샘플링 모드. `resMode=`의 기본값입니다. 렌더링된 이미지의 크기를 최종 크기로 조정하는 데 사용되는 재샘플링 및 보간 특성을 지정합니다.

## 속성 {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

열거형. `'bilin'`의 경우 2, `'bicub'`의 경우 3 또는 `'sharp2'` 보간 모드의 경우 4로 설정합니다(자세한 내용은 [resMode=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md) 참조).

## 기본값 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

정의되지 않았거나 비어 있는 경우 `default::ResMode`에서 상속됩니다.

## 참조 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)

