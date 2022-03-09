---
description: 레이어 보기 속성
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 12%

---

# LayerViewInfo{#layerviewinfo}

레이어 보기 속성

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| url | `xsd:string` | 템플릿을 나타내는 이미지 서버 URL입니다. 결합 `urlModifier` 및 `urlPostAp- plyModifier` 필드. |
| urlModifier | `xsd:string` | 요청 또는 실행 전에 적용할 이미지 제공 프로토콜 명령 `urlPostApplyModifier` 명령. |
| urlPostApplyModifier | `xsd:string` | 이후에 적용할 이미지 제공 프로토콜 명령 `urlModifier` 및 요청 명령 |
