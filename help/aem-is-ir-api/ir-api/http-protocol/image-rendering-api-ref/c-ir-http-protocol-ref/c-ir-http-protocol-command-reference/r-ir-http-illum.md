---
description: 조명 맵 선택기입니다. 이 자료를 렌더링할 대상 조명 맵을 지정합니다.
seo-description: 조명 맵 선택기입니다. 이 자료를 렌더링할 대상 조명 맵을 지정합니다.
seo-title: 실음
solution: Experience Manager
title: 실음
topic: Scene7 Image Serving - Image Rendering API
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 4%

---


# ilum{#illum}

조명 맵 선택기입니다. 이 자료를 렌더링할 대상 조명 맵을 지정합니다.

`illum=-1|0|1|2`

지정된 조명 맵을 대상 비네팅에서 사용할 수 없는 경우 가장 가까운 사용 가능한 맵이 대신 사용됩니다.

`illum=-1` 값을 기반으로 조명 맵이 자동으로 선택되도록  `gloss=` 지정합니다.

## 속성 {#section-aace8466566e4cf1a0c5a6c0167245c9}

재료 속성. 비네팅이 여러 조명 맵을 정의하지 않으면 무시됩니다.

## 기본값 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 참조 {#section-9132e60381c64aa3a8ed1319690db55e}

[광택=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
