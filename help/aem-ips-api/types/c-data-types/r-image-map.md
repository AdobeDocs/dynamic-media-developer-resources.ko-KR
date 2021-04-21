---
description: Target을 참조하십시오.
solution: Experience Manager
title: 이미지 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 12%

---


# 이미지 맵{#imagemap}

Target을 참조하십시오.

항상 이미지와 연결되어 있습니다. `ImageInfo`에서 `ImageMap` 타겟을 가져올 수 있습니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 이미지 맵 핸들. |
| `*`name`*` | `xsd:string` | 이미지 맵 이름입니다. |
| `*`지역`*` | `xsd:string` | 이미지 맵 좌표. 형식은 HTML `<area>` 태그 속성을 기반으로 합니다. |
| `*`작업	`*` | `xsd:string` | `href` URL을 포함하여 HTML `<area>` 태그에 포함할 다른 속성입니다. |
| `*`shapeType`*` | `xsd:boolean` | [!DNL RegionShape] 값입니다. |
| `*`위치`*` | `xsd:string` | HTML `<area>` 요소의 [!DNL coords] 특성 형식의 위치입니다. 예: `coords ="0,0,84,128"`. |
| `*`활성화됨`*` | `xsd:boolean` | 이미지 맵이 활성화되어 있으면 true입니다. |
| `*`lastModified`*` | `xsd:dateTime` | 이미지 맵을 마지막으로 수정한 날짜 및 시간입니다. |

