---
description: 브라우저에서 클릭 동작에 대한 Target.
solution: Experience Manager
title: 이미지 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 12%

---

# 이미지 맵{#imagemap}

브라우저에서 클릭 동작에 대한 Target.

항상 이미지와 연결되어 있습니다. `ImageInfo`에서 `ImageMap` 타겟을 가져올 수 있습니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 이미지 맵 핸들. |
| `*`name`*` | `xsd:string` | 이미지 맵 이름입니다. |
| `*`지역`*` | `xsd:string` | 이미지 맵 좌표입니다. 형식은 HTML `<area>` 태그 속성을 기반으로 합니다. |
| `*`작업	`*` | `xsd:string` | `href` URL을 포함하여 HTML `<area>` 태그에 포함할 다른 속성입니다. |
| `*`shapeType`*` | `xsd:boolean` | [!DNL RegionShape] 값. |
| `*`위치`*` | `xsd:string` | HTML `<area>` 요소의 [!DNL coords] 속성 형식으로 배치합니다. 예: `coords ="0,0,84,128"`. |
| `*`활성화됨`*` | `xsd:boolean` | 이미지 맵이 활성화되어 있으면 True입니다. |
| `*`lastModified`*` | `xsd:dateTime` | 이미지 맵을 마지막으로 수정한 날짜 및 시간입니다. |
