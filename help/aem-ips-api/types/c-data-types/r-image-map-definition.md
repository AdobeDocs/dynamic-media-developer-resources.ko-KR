---
description: 브라우저에서 클릭 작업에 대한 Target 정의.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 12%

---

# ImageMapDefinition{#imagemapdefinition}

브라우저에서 클릭 작업에 대한 Target 정의.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 이름 | `xsd:string` | 이미지 맵 정의의 이름입니다. |
| shapeType | `xsd:string` | 영역 모양 값 중 하나입니다. |
| 지역 | `xsd:string` | 이미지 맵 좌표입니다. 형식은 HTML을 기반으로 합니다 `<area>` 태그 속성을 사용합니다. |
| 작업	 | `xsd:string` | HTML에 포함할 다른 속성 `<area>` 태그( `href` URL. |
| 활성화됨 | `xsd:boolean` | 이미지 맵이 활성화되어 있으면 True입니다. |
