---
description: 브라우저에서 클릭 작업에 대한 Target 정의.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 11%

---

# ImageMapDefinition{#imagemapdefinition}

브라우저에서 클릭 작업에 대한 Target 정의.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`name`*` | `xsd:string` | 이미지 맵 정의의 이름입니다. |
| `*`shapeType`*` | `xsd:string` | 영역 모양 값 중 하나입니다. |
| `*`지역`*` | `xsd:string` | 이미지 맵 좌표입니다. 형식은 HTML `<area>` 태그 속성을 기반으로 합니다. |
| `*`작업	`*` | `xsd:string` | `href` URL을 포함하여 HTML `<area>` 태그에 포함할 다른 속성입니다. |
| `*`활성화됨`*` | `xsd:boolean` | 이미지 맵이 활성화되어 있으면 True입니다. |
