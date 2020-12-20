---
description: 브라우저의 클릭 동작에 대한 Target 정의입니다.
seo-description: 브라우저의 클릭 동작에 대한 Target 정의입니다.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Scene7 Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 10%

---


# ImageMapDefinition{#imagemapdefinition}

브라우저의 클릭 동작에 대한 Target 정의입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`name`*` | `xsd:string` | 이미지 맵 정의의 이름입니다. |
| ` *`shapeType`*` | `xsd:string` | 영역 모양 값 중 하나입니다. |
| ` *`지역`*` | `xsd:string` | 이미지 맵 좌표. 형식은 HTML `<area>` 태그 속성을 기반으로 합니다. |
| ` *`작업	`*` | `xsd:string` | `href` URL을 포함하여 HTML `<area>` 태그에 포함할 다른 속성입니다. |
| ` *`활성화됨`*` | `xsd:boolean` | 이미지 맵이 활성화되어 있으면 true입니다. |

