---
description: IS는 HTML 이미지 맵의 사용을 단순화하는 메커니즘을 제공합니다. IS의 JAVA 기반 및 Flash 기반 뷰어에는 이미지 맵에 대한 제한된 지원도 포함됩니다.
solution: Experience Manager
title: 이미지 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# 이미지 맵{#image-maps}

IS는 HTML 이미지 맵의 사용을 단순화하는 메커니즘을 제공합니다. IS의 JAVA 기반 및 Flash 기반 뷰어에는 이미지 맵에 대한 제한된 지원도 포함됩니다.

Source 이미지 맵은 `catalog::Map` 또는 `map=` 명령을 사용하여 IS에 제공되며 처리된 맵은 `req=map` 명령을 사용하여 검색됩니다.

이미지 맵은 &#39;&lt;&#39; 및 &#39;>&#39;로 올바르게 구분된 하나 이상의 HTML AREA 요소로 구성됩니다. catalog::Map을 통해 제공되는 경우 모든 픽셀 좌표 값은 원본 이미지 해상도이며 수정되지 않은 소스 이미지의 왼쪽 상단 모서리에 상대적인 것으로 간주됩니다. `map=` 명령을 통해 제공된 경우 좌표 값은 레이어의 왼쪽 위 모퉁이를 기준으로 한 레이어 좌표로 간주됩니다(`rotate=` 및 `extend=` 이후).

>[!NOTE]
>
>% 좌표는 현재 허용되지 않으며 잘못 처리될 수 있습니다.

IS는 맵 좌표에 공간 변환(예: 스케일링 및 회전)을 적용한 다음 처리된 레이어 맵을 적절한 z-차수(전후)로 적절한 위치로 조합하여 각 구성 레이어의 소스 이미지 맵으로부터 합성 이미지 맵을 생성합니다.

다음 명령은 `req=map`과(와) 함께 제공된 경우(요청에서 직접, 카탈로그 템플릿을 통해 또는 `catalog::Modifier` 문자열에서) 이미지 맵 처리용으로 고려됩니다.

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

`req=map` 요청을 처리하는 동안 `AREA`의 `SHAPE` 및 `COORDS` 특성을 수정할 수 있습니다. `AREA` 요소의 다른 모든 특성은 수정 없이 전달됩니다. 대부분의 경우 `SHAPE` 값을 `DEFAULT`에서 `RECT`(으)로 변경하거나(`COORDS` 특성도 추가함) `COORDS` 값을 변경합니다.

처리하는 동안 비어 있는 모든 `AREA` 요소는 완전히 제거됩니다. 맵이 `layer=comp`과(와) 연결되어 있으면 다른 모든 맵 뒤에 배치됩니다. 하나 이상의 HTML `AREA` 요소로 데이터가 텍스트 형식으로 반환됩니다. 빈 응답 문자열은 지정된 개체에 대한 이미지 맵이 없음을 나타냅니다.

맵 처리에는 레이어 투명도가 고려되지 않습니다. 완전히 투명한 레이어는 여전히 그와 연관된 이미지 맵을 가질 수 있다. 부분 투명 레이어의 맵은 투명 영역에 클리핑되지 않습니다.

## 참조 {#see-also}

[맵=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [카탈로그::맵](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 사양](https://www.w3.org/TR/html401/)
