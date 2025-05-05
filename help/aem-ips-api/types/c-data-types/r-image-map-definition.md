---
description: 브라우저에서 클릭 동작에 대한 대상 정의입니다.
solution: Experience Manager
title: 이미지 맵 정의
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

브라우저에서 클릭 동작에 대한 대상 정의입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| name | `xsd:string` | 이미지 맵 정의의 이름입니다. |
| shapeType | `xsd:string` | 영역 셰이프 값 중 하나. |
| 지역 | `xsd:string` | 이미지 맵 좌표. 형식은 HTML `<area>` 태그 특성을 기반으로 합니다. |
| 작업  | `xsd:string` | `href` URL을 포함하여 HTML `<area>` 태그에 포함할 기타 특성입니다. |
| 활성화됨 | `xsd:boolean` | 이미지 맵이 활성화된 경우 True입니다. |
