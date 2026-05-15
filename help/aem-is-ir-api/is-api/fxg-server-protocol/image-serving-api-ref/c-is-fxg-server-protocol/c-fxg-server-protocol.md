---
title: FXG 서버 프로토콜
description: 그래픽을 조작하려면 나침반 지점과 비슷한 참조 지점을 사용할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: 'https://experienceleague.adobe.com/DXmhIshiUYoP-BlVe5cJFXbII9sEIdyo5YDkoKP-t0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 28%

---

# FXG 서버 프로토콜{#fxg-server-protocol}

그래픽을 조작하려면 나침반 지점과 비슷한 참조 지점을 사용할 수 있습니다.

참조 지점을 사용할 경우 특정 참조 지점을 기준으로 그래픽을 회전하거나 배율 또는 크기를 조정할 수 있습니다. 참조 지점은 `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` 및 `southeast`입니다. 예를 들어 중심 참조점을 사용하여 그래픽을 중심에서 45° 회전할 수 있습니다. 다음 이미지는 참조점이 있는 위치, 그래픽, 해당 `northWest` 참조점에서 20도 회전된 그래픽 및 해당 `east` 참조점에서 20도 회전된 그래픽을 보여 줍니다.

![참조 지점 이미지](assets/wp_ref_points.png)

* A. 참조점 위치
* B 그래픽
* C. 그래픽이 `northWest` 기준점에서 20° 회전되었습니다.
* D. 그래픽이 `east` 기준점에서 20° 회전되었습니다.

구문은 다음과 같습니다.

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

기본값은 none입니다. `inherit` 값은 `none`이(가) 아닌 경우 페이지 또는 그룹 수준의 맨 위에서 모든 하위 항목에 `s7:referencePoint` 값을 전달합니다. `none` 설정은 개체에 대한 참조점이 없으며 FXG 좌표계가 사용됨을 의미합니다.

>[!NOTE]
>
>참조 지점을 사용하고 조작 후 개체에 위치 이동이 없도록 하려면 개체를 조작한 후 개체의 x 및 y 값을 업데이트합니다.

`s7:referencePoint`의 값을 그룹(또는 경로, 선 요소 또는 명확한 너비 및 높이 정의가 없는 요소)과 함께 사용하면 값이 그룹의 누적 경계 상자에 적용됩니다. 예를 들어, 그룹에 있는 모든 개체의 테두리 상자 왼쪽 위 점이 그룹의 `northWest` 참조점 역할을 하고 오른쪽 아래 점이 `southEast` 참조점 역할을 합니다.
