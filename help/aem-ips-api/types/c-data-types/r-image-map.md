---
description: 브라우저에서 클릭 동작에 대해 타깃팅합니다.
seo-description: 브라우저에서 클릭 동작에 대해 타깃팅합니다.
seo-title: 이미지 맵
solution: Experience Manager
title: 이미지 맵
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 이미지 맵{#imagemap}

브라우저에서 클릭 동작에 대해 타깃팅합니다.

항상 이미지와 연결되어 있습니다. 타겟을 `ImageMap` 얻을 수 `ImageInfo`있습니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | 이미지 맵 핸들 |
| ` *`name`*` | `xsd:string` | 이미지 맵 이름입니다. |
| ` *`지역`*` | `xsd:string` | 이미지 맵 좌표. 형식은 HTML `<area>` 태그 속성을 기반으로 합니다. |
| ` *`작업	`*` | `xsd:string` | URL을 포함하여 HTML `<area>` 태그에 포함할 다른 `href` 속성입니다. |
| ` *`shapeType`*` | `xsd:boolean` | A [!DNL RegionShape] 값. |
| ` *`위치`*` | `xsd:string` | HTML `<area>` 요소의 [!DNL coords] 속성 형식으로 배치합니다. 예: `coords ="0,0,84,128"`. |
| ` *`활성화됨`*` | `xsd:boolean` | 이미지 맵이 활성화되어 있으면 true입니다. |
| ` *`lastModified`*` | `xsd:dateTime` | 이미지 맵을 마지막으로 수정한 날짜 및 시간입니다. |

