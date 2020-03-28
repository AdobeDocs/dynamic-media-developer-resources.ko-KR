---
description: IS는 HTML 이미지 맵 사용을 단순화하는 메커니즘을 제공합니다. IS의 JAVA 기반 뷰어와 Flash 기반 뷰어에는 이미지 맵에 대한 지원이 제한됩니다.
seo-description: IS는 HTML 이미지 맵 사용을 단순화하는 메커니즘을 제공합니다. IS의 JAVA 기반 뷰어와 Flash 기반 뷰어에는 이미지 맵에 대한 지원이 제한됩니다.
seo-title: 이미지 맵
solution: Experience Manager
title: 이미지 맵
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Image maps{#image-maps}

IS는 HTML 이미지 맵 사용을 단순화하는 메커니즘을 제공합니다. IS의 JAVA 기반 뷰어와 Flash 기반 뷰어에는 이미지 맵에 대한 지원이 제한됩니다.

소스 이미지 맵은 명령을 통해 `catalog::Map` 또는 명령을 통해 IS에 제공되며, 처리된 맵은 `map=` `req=map` 명령을 사용하여 검색됩니다.

이미지 맵은 &#39;&lt;&#39; 및 &#39;>&#39;로 적절하게 구분된 하나 이상의 HTML AREA 요소로 구성됩니다. catalog::Map을 통해 제공되는 경우 모든 픽셀 좌표 값은 원본 이미지 해상도에 있고 (수정되지 않은) 소스 이미지의 왼쪽 위 모서리를 기준으로 한다고 가정합니다. 명령을 통해 제공되는 `map=` 경우 좌표 값은 레이어의 왼쪽 위 모서리를 기준으로 하는 레이어 좌표로 `rotate=` 간주됩니다(뒤 및 `extend=`).

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>% 좌표는 현재 허용되지 않으며 잘못 처리될 수 있습니다.

IS는 맵 좌표에 공간 변형(크기 조절 및 회전 등)을 적용한 다음 처리된 레이어 맵을 적절한 z-순서(앞뒤)와 적절한 위치에 조합하여 각 구성 레이어의 소스 이미지 맵에서 합성 이미지 맵을 생성합니다.

다음 명령은 요청에서 직접, 카탈로그 템플릿을 통해 `req=map` 또는 `catalog::Modifier` 문자열을 통해 제공되면 이미지 맵 처리에 대해 고려됩니다.

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

요청의 `SHAPE` 및 `COORDS` 속성은 `AREA` 처리 중에 수정할 `req=map` `AREA` 수 있으며, 요소의 다른 모든 속성은 수정 없이 전달됩니다. 대부분의 경우 이 작업에는 `SHAPE` 값을 에서 `DEFAULT` 로 `RECT` 변경하거나( `COORDS` 속성을 추가하기도 함) `COORDS` 값을 변경하는 작업이 포함됩니다.

처리 중에 비어 있는 모든 `AREA` 요소는 완전히 제거됩니다. 지도가 연결되어 있으면 다른 모든 지도 뒤에 `layer=comp` 배치됩니다. 데이터는 하나 이상의 HTML `AREA` 요소로 텍스트 형식으로 반환됩니다. 빈 답글 문자열은 지정된 개체에 대한 이미지 맵이 없음을 나타냅니다.

맵 처리에서는 레이어 투명도가 고려되지 않습니다. 완전히 투명한 레이어에도 이미지 맵이 연결되어 있을 수 있습니다. 부분적으로 투명한 레이어의 맵은 투명 영역으로 잘리지 않습니다.

## 참조 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 사양](http://www.w3.org/TR/html401/)
