---
title: illum
description: 조명 맵 선택기. 이 재료가 렌더링되는 데 선호하는 조명 맵을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 3%

---

# illum{#illum}

조명 맵 선택기. 이 재료가 렌더링되는 데 선호하는 조명 맵을 지정합니다.

`illum=-1|0|1|2`

대상 비네팅에서 지정된 조명 맵을 사용할 수 없는 경우 가장 가까운 사용 가능한 맵이 대신 사용됩니다.

`illum=-1` 조명 맵이 다음을 기준으로 자동으로 선택되도록 지정합니다. `gloss=` 값.

## 속성 {#section-aace8466566e4cf1a0c5a6c0167245c9}

재질 속성입니다. 비네팅에서 여러 조명 맵을 정의하지 않는 경우에는 무시됩니다.

## 기본값 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 참조 {#section-9132e60381c64aa3a8ed1319690db55e}

[광택=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
