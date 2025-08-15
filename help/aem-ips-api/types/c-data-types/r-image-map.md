---
description: 브라우저에서 클릭 동작에 대한 Target입니다.
solution: Experience Manager
title: 이미지 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

브라우저에서 클릭 동작에 대한 Target입니다.

항상 이미지와 연결됩니다. `ImageMap`에서 `ImageInfo` 대상을 가져올 수 있습니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 이미지 맵 핸들 | `xsd:string` | 이미지 맵 핸들입니다. |
| [!DNL name] | `xsd:string` | 이미지 맵 이름. |
| [!DNL region] | `xsd:string` | 이미지 맵 좌표. 형식은 HTML `<area>` 태그 특성을 기반으로 합니다. |
| [!DNL action] | `xsd:string` | `<area>` URL을 포함하여 HTML `href` 태그에 포함할 기타 특성입니다. |
| shapeType | `xsd:boolean` | [!DNL RegionShape] 값. |
| [!DNL position] | `xsd:string` | HTML `<area>` 요소의 [!DNL coords] 특성 형식으로 위치를 지정합니다. 예: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | 이미지 맵이 활성화된 경우 True입니다. |
| 마지막 수정일 | `xsd:dateTime` | 이미지 맵을 마지막으로 수정한 날짜 및 시간입니다. |
