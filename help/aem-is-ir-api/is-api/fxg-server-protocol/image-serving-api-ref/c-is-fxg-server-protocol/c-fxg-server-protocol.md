---
description: 그래픽을 조작하려면 나침반 지점과 비슷한 참조 지점을 사용할 수 있습니다.
seo-description: 그래픽을 조작하려면 나침반 지점과 비슷한 참조 지점을 사용할 수 있습니다.
seo-title: FXG 서버 프로토콜
solution: Experience Manager
title: FXG 서버 프로토콜
topic: Scene7 Image Serving - Image Rendering API
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 65%

---


# FXG 서버 프로토콜{#fxg-server-protocol}

그래픽을 조작하려면 나침반 지점과 비슷한 참조 지점을 사용할 수 있습니다.

참조 지점을 사용할 경우 특정 참조 지점을 기준으로 그래픽을 회전하거나 배율 또는 크기를 조정할 수 있습니다. 참조점은 `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` 및 `southeast`입니다. 예를 들어 가운데 참조 지점을 사용하면 가운데를 기준으로 그래픽을 45도만큼 회전할 수 있습니다. 이 그림은 참조점의 위치, 그래픽, `northWest` 참조점에서 20도 회전된 그래픽 및 `east` 참조점에서 20도 회전한 그래픽을 보여줍니다.

![](assets/wp_ref_points.png)

* A. 참조 지점 위치
* B. A 그래픽
* C. 그래픽이 `northWest` 참조점에서 20도 회전합니다.
* D. 그래픽이 `east` 참조점에서 20도 회전합니다.

구문은 다음과 같습니다.

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

기본값은 none입니다. `inherit` 값은 `s7:referencePoint`이 아닌 경우 페이지 상단 또는 그룹 수준에서 모든 하위 항목까지 `none` 값을 전달합니다. `none` 설정은 개체의 참조 지점이 없으며 FXG 좌표계가 사용됨을 나타냅니다.

>[!NOTE]
>
>참조 지점을 사용하고 조작 후 개체에 위치 이동이 없도록 하려면 개체를 조작한 후 개체의 x 및 y 값을 업데이트합니다.

`s7:referencePoint`에서의 값을 그룹(또는 경로, 라인 요소 또는 명시적 너비 및 높이 정의가 없는 모든 요소)에 사용하는 경우 그룹의 누적 경계 상자에 값이 적용됩니다. 예를 들어 그룹의 모든 개체의 테두리 상자의 왼쪽 위 점은 그룹의 `northWest` 참조 포인트 역할을 합니다.오른쪽 아래 점은 `southEast` 참조 포인트 역할을 합니다.

