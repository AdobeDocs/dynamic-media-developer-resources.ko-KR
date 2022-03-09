---
description: 브라우저에서 클릭 동작에 대한 Target.
solution: Experience Manager
title: 이미지 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 13%

---

# 이미지 맵{#imagemap}

브라우저에서 클릭 동작에 대한 Target.

항상 이미지와 연결되어 있습니다. ID를 얻을 수 있습니다 `ImageMap` 타겟 `ImageInfo`.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| imageMapHandle | `xsd:string` | 이미지 맵 핸들. |
| 이름 | `xsd:string` | 이미지 맵 이름입니다. |
| 지역 | `xsd:string` | 이미지 맵 좌표입니다. 형식은 HTML을 기반으로 합니다 `<area>` 태그 속성을 사용합니다. |
| 작업	 | `xsd:string` | HTML에 포함할 다른 속성 `<area>` 태그( `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] 값. |
| position | `xsd:string` | HTML 형식으로 위치 `<area>` 요소 [!DNL coords] 속성을 사용합니다. For example: `coords ="0,0,84,128"`. |
| 활성화됨 | `xsd:boolean` | 이미지 맵이 활성화되어 있으면 True입니다. |
| lastModified | `xsd:dateTime` | 이미지 맵을 마지막으로 수정한 날짜 및 시간입니다. |
