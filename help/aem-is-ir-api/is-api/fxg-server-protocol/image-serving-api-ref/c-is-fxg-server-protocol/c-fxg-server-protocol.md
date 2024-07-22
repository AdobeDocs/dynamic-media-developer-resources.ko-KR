---
title: FXG 서버 프로토콜
description: 그래픽을 조작하려면 나침반 점과 유사한 참조 점을 사용할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 18%

---

# FXG 서버 프로토콜{#fxg-server-protocol}

그래픽을 조작하려면 나침반 점과 유사한 참조 점을 사용할 수 있습니다.

참조 지점을 사용할 경우 특정 참조 지점을 기준으로 그래픽을 회전하거나 배율 또는 크기를 조정할 수 있습니다. 참조 지점은 `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` 및 `southeast`입니다. 예를 들어 중심 참조점을 사용하여 그래픽을 중심에서 45° 회전할 수 있습니다. 다음 이미지는 참조점이 있는 위치, 그래픽, 해당 `northWest` 참조점에서 20도 회전된 그래픽 및 해당 `east` 참조점에서 20도 회전된 그래픽을 보여 줍니다.

![참조 지점 이미지](assets/wp_ref_points.png)

* A. 참조점 위치
* B. 그래픽
* C. 그래픽이 `northWest` 기준점에서 20° 회전되었습니다.
* D. 그래픽이 `east` 기준점에서 20° 회전되었습니다.

구문은 다음과 같습니다.

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

기본값은 none입니다. `inherit` 값은 `none`이(가) 아닌 경우 페이지 또는 그룹 수준의 맨 위에서 모든 하위 항목에 `s7:referencePoint` 값을 전달합니다. `none` 설정은 개체에 대한 참조점이 없으며 FXG 좌표계가 사용됨을 의미합니다.

>[!NOTE]
>
>참조 지점을 사용하고 조작 후 개체에 위치 이동이 없도록 하려면 개체를 조작한 후 개체의 x 및 y 값을 업데이트합니다.

`s7:referencePoint`의 값을 그룹(또는 경로, 선 요소 또는 명확한 너비 및 높이 정의가 없는 요소)과 함께 사용하면 값이 그룹의 누적 경계 상자에 적용됩니다. 예를 들어, 그룹에 있는 모든 개체의 테두리 상자 왼쪽 위 점이 그룹의 `northWest` 참조점 역할을 하고 오른쪽 아래 점이 `southEast` 참조점 역할을 합니다.
