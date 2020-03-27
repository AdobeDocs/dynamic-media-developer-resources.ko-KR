---
description: 이미지 맵 데이터. HTML <AREA> 요소 중 하나 이상의 전체 HTML 요소를 포함하지 않습니다.
seo-description: 이미지 맵 데이터. HTML <AREA> 요소 중 하나 이상의 전체 HTML 요소를 포함하지 않습니다.
seo-title: 맵
solution: Experience Manager
title: 맵
topic: Scene7 Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 맵{#map}

이미지 맵 데이터. HTML 요소 없음, 앞뒤로 정렬된 전체 `<AREA>` HTML 요소

서버가 SHAPE 및 COORDS 속성을 해석하고 변경할 수 있습니다. (SHAPE=CIRCLE은 이 릴리스에서 지원되지 않습니다.) 다른 모든 속성은 수정 없이 `<AREA>` 전달됩니다. COORDS 특성으로 지정된 좌표 값은 수정되지 않은 소스 이미지의 왼쪽 위 모서리에서 픽셀 오프셋이어야 합니다. (`%` 좌표는 이번 릴리스에서 지원되지 않으며 제대로 처리되지 않을 수 있습니다.)

## 속성 {#section-f52d89fd399b4356ac05277e6c12f956}

텍스트 문자열 값. 지정된 경우 하나 이상의 전체 HTML `<AREA>` 요소여야 합니다.

이 필드는 텍스트 문자열 현지화에 참여하고 있습니다. 자세한 내용은 [HTTP 프로토콜](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 참조 *문서의 텍스트 문자열 현지화를* 참조하십시오.

## 기본값 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

없음.

## 참조 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [텍스트 문자열 현지화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
