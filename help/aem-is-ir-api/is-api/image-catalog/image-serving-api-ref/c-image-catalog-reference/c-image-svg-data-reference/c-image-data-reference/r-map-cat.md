---
description: 이미지 맵 데이터. 완료 HTML 없음 또는 이상 <area> 전면에서 후면으로 정렬된 요소.
solution: Experience Manager
title: 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# 맵{#map}

이미지 맵 데이터. 완료 HTML 없음 또는 이상 `<AREA>` 전면에서 후면으로 정렬된 요소.

서버에서 SHAPE 및 COORDS 속성을 해석하고 변경할 수 있습니다. (SHAPE=CIRCLE은 이 릴리스에서 지원되지 않습니다.) 의 기타 모든 속성 `<AREA>` 수정 없이 전달됩니다. COORDS 속성으로 지정된 좌표 값은 수정되지 않은 소스 이미지의 왼쪽 상단 모서리에서 픽셀 오프셋이어야 합니다. (`%` 좌표는 이 릴리스에서 지원되지 않으므로 올바르게 처리되지 않을 수 있습니다.)

## 속성 {#section-f52d89fd399b4356ac05277e6c12f956}

텍스트 문자열 값입니다. 지정하면 하나 이상의 완전한 HTML이 되어야 합니다. `<AREA>` 요소.

이 필드는 텍스트 문자열 현지화에 적용됩니다. 을(를) 참조하십시오 [텍스트 문자열 로컬라이제이션](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 다음에서 *HTTP 프로토콜 참조* 을 참조하십시오.

## 기본값 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

없음.

## 참조 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [텍스트 문자열 로컬라이제이션](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
