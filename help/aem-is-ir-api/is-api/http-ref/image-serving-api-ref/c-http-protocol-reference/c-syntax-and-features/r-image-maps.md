---
description: IS는 HTML 이미지 맵의 사용을 단순화하는 메커니즘을 제공합니다. IS의 JAVA 기반 및 Flash 기반 뷰어에는 이미지 맵에 대한 제한된 지원도 포함됩니다.
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

IS는 HTML 이미지 맵의 사용을 단순화하는 메커니즘을 제공합니다. IS의 JAVA 기반 및 Flash 기반 뷰어에는 이미지 맵에 대한 제한된 지원도 포함됩니다.

소스 이미지 맵은 다음을 통해 IS에 제공됩니다. `catalog::Map` 또는 `map=` 명령 및 처리된 맵은 `req=map` 명령입니다.

이미지 맵은 &#39;&lt;&#39; 및 &#39;>&#39;로 올바르게 구분된 하나 이상의 HTML AREA 요소로 구성됩니다. catalog::Map 을 통해 제공되는 경우 모든 픽셀 좌표 값은 원본 이미지 해상도이며 수정되지 않은 소스 이미지의 왼쪽 상단 모서리에 상대적인 것으로 간주됩니다. 를 통해 제공되는 경우 `map=` 명령에서 좌표 값은 레이어의 왼쪽 위 모서리를 기준으로 레이어 좌표로 간주됩니다(다음 항목 뒤) `rotate=` 및 `extend=`).

>[!NOTE]
>
>% 좌표는 현재 허용되지 않으며 잘못 처리될 수 있습니다.

IS는 맵 좌표에 공간 변환(예: 스케일링 및 회전)을 적용한 다음 처리된 레이어 맵을 적절한 z-차수(전후)로 적절한 위치로 조합하여 각 구성 레이어의 소스 이미지 맵으로부터 합성 이미지 맵을 생성합니다.

다음 명령은 와 함께 제공될 때 이미지 맵 처리에 고려됩니다. `req=map` (요청에서 직접, 카탈로그 템플릿을 통해 또는 `catalog::Modifier` 문자열):

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

다음 `SHAPE` 및 `COORDS` 의 속성 `AREA` 을(를) 처리하는 동안 변경될 수 있습니다. `req=map` 요청, 의 다른 모든 속성 `AREA` 요소는 수정 없이 전달됩니다. 대부분의 경우 다음과 같이 변경됩니다. `SHAPE` 값: 부터 `DEFAULT` 끝 `RECT` (또한 `COORDS` attribute) 또는 `COORDS` 값.

임의 `AREA` 처리 중에 비어 있는 요소는 완전히 제거됩니다. 맵이 연결된 경우 `layer=comp` 다른 모든 지도 뒤에 있습니다. 데이터는 하나 이상의 HTML 형태로 텍스트 형식으로 반환됩니다 `AREA` 요소. 빈 응답 문자열은 지정된 개체에 대한 이미지 맵이 없음을 나타냅니다.

맵 처리에는 레이어 투명도가 고려되지 않습니다. 완전히 투명한 레이어는 여전히 그와 연관된 이미지 맵을 가질 수 있다. 부분적으로 투명한 레이어의 맵은 투명 영역에 클리핑되지 않습니다.

## 참조 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 사양](https://www.w3.org/TR/html401/)
