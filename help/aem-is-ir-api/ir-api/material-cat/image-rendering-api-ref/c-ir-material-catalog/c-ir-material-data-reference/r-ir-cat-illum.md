---
description: 조명 맵 선택기. 이 재료를 렌더링할 때 사용할 조명 맵을 명시적으로 선택할 수 있습니다.
solution: Experience Manager
title: 일럼
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e74b3e8-6289-4114-aa11-a6f91671363e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# 일럼{#illum}

조명 맵 선택기. 이 재료를 렌더링할 때 사용할 조명 맵을 명시적으로 선택할 수 있습니다.

## 속성 {#section-162bcf562ca844ccba9e81e267508cca}

열거형. catalog::Gloss 값을 기준으로 조명 맵을 자동으로 선택하려면 -1로 설정합니다.

조명 맵 A, B 또는 C를 선택하려면 0, 1 또는 2로 설정합니다. 렌더러는 비네팅에서 사용할 수 있는 가장 가까운 조명 맵을 선택합니다.

## 기본값 {#section-ac386d31ef90423b8a367010a60bddc7}

-1(자동 선택)

## 참조 {#section-d9db8507a5e54692b84f54b3f84b782a}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)
