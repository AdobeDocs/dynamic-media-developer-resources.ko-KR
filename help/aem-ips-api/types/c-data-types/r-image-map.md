---
description: 브라우저에서 클릭 동작에 대한 Target.
solution: Experience Manager
title: 이미지 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 6%

---

# [!DNL ImageMap]{#imagemap}

브라우저에서 클릭 동작에 대한 Target.

항상 이미지와 연결됩니다. 다음을 얻을 수 있습니다. `ImageMap` 대상 출처: `ImageInfo`.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 이미지 맵 핸들 | `xsd:string` | 이미지 맵 핸들입니다. |
| [!DNL name] | `xsd:string` | 이미지 맵 이름. |
| [!DNL region] | `xsd:string` | 이미지 맵 좌표. 형식은 HTML을 기반으로 합니다. `<area>` 태그 속성입니다. |
| [!DNL action] | `xsd:string` | HTML에 포함할 기타 속성 `<area>` 태그(다음을 포함) `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] 값. |
| [!DNL position] | `xsd:string` | HTML 형식의 위치 `<area>` 요소 [!DNL coords] 특성. 예: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | 이미지 맵이 활성화된 경우 True입니다. |
| 마지막 수정일 | `xsd:dateTime` | 이미지 맵을 마지막으로 수정한 날짜 및 시간입니다. |
