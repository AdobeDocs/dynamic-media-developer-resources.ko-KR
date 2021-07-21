---
description: 레이어 보기 속성
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 11%

---

# LayerViewInfo{#layerviewinfo}

레이어 보기 속성

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`url`*` | `xsd:string` | 템플릿을 나타내는 이미지 서버 URL입니다. `urlModifier` 필드와 `urlPostAp- plyModifier` 필드를 결합합니다. |
| `*`urlModifier`*` | `xsd:string` | 요청 또는 `urlPostApplyModifier` 명령 전에 적용할 이미지 제공 프로토콜 명령입니다. |
| `*`urlPostApplyModifier`*` | `xsd:string` | `urlModifier` 및 요청 명령 다음에 적용할 이미지 제공 프로토콜 명령입니다. |
