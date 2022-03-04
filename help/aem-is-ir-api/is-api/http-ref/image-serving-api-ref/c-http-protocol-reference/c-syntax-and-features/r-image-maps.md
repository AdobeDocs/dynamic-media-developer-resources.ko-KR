---
description: IS는 HTML 이미지 맵 사용을 간소화하는 메커니즘을 제공합니다. IS의 JAVA 기반 및 Flash 기반 뷰어에는 이미지 맵에 대한 제한된 지원도 포함되어 있습니다.
solution: Experience Manager
title: 이미지 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 이미지 맵{#image-maps}

IS는 HTML 이미지 맵 사용을 간소화하는 메커니즘을 제공합니다. IS의 JAVA 기반 및 Flash 기반 뷰어에는 이미지 맵에 대한 제한된 지원도 포함되어 있습니다.

소스 이미지 맵은 를 통해 IS에 제공됩니다 `catalog::Map` 또는 `map=` 명령 및 처리된 맵은 `req=map` 명령.

이미지 맵은 &#39;&lt;&#39; 및 &#39;>&#39;로 적절히 구분된 하나 이상의 HTML AREA 요소로 구성됩니다. 카탈로그를 통해 제공되는 경우:Map에서는 모든 픽셀 좌표 값이 원본 이미지 해상도에 있고 (수정되지 않은) 소스 이미지의 왼쪽 위 모서리에 상대적인 것으로 간주됩니다. 를 통해 제공되는 경우 `map=` 명령을 실행하면 좌표 값은 레이어의 왼쪽 위 모서리를 기준으로 레이어 좌표로 간주됩니다(뒤에 있음) `rotate=` 및 `extend=`).

>[!NOTE]
>
>% 좌표는 현재 허용되지 않으며 잘못 처리될 수 있습니다.

IS는 각 구성 레이어의 소스 이미지 맵에서 공간 변형(크기 조절 및 회전 등)을 맵 좌표에 적용한 다음, 처리된 레이어 맵을 적절한 z-순서(전후)와 적절한 위치로 조립하여 복합 이미지 맵을 생성합니다.

다음 명령은 와 함께 제공되는 경우 이미지 맵 처리용으로 간주됩니다 `req=map` (요청에서 직접, 카탈로그 템플릿을 통해 또는 `catalog::Modifier` 문자열):

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

다른 모든 명령은 효과적으로 무시됩니다.

다음 `SHAPE` 및 `COORDS` 속성 `AREA` 는 `req=map` 요청, 기타 모든 속성 `AREA` 요소는 수정 없이 전달됩니다. 대부분의 경우 이 작업에는 `SHAPE` 값: `DEFAULT` to `RECT` ( 또한 `COORDS` 속성) 또는 `COORDS` 값.

임의 `AREA` 처리 중에 비어 있는 요소가 완전히 제거됩니다. 맵이 `layer=comp` 그것은 다른 모든 지도 뒤에 놓여져 있다. 데이터가 하나 이상의 HTML으로 텍스트 양식으로 반환됩니다 `AREA` 요소를 생성하지 않습니다. 빈 회신 문자열은 지정된 개체에 대해 이미지 맵이 없음을 나타냅니다.

레이어 투명도는 맵 처리에서 고려되지 않습니다. 완전히 투명한 레이어에는 이미지 맵이 연결되어 있을 수 있습니다. 부분적으로 투명한 레이어의 맵은 투명 영역에 클리핑되지 않습니다.

## 참조 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [카탈로그::맵](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 사양](https://www.w3.org/TR/html401/)
