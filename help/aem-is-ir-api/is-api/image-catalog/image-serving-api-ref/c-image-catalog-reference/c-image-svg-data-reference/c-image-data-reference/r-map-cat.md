---
description: 이미지 맵 데이터. 앞쪽에서 뒤로 정렬된 완전한 HTML <AREA> 요소가 하나 이상 없습니다.
solution: Experience Manager
title: 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
TQID: 'https://experienceleague.adobe.com/JY0barcvbF72sTyYW4iIhjFE-8tfqtbI78PDccLcXV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 2%

---

# 맵{#map}

이미지 맵 데이터. 앞쪽에서 뒤로 정렬된 완전한 HTML `<AREA>` 요소가 하나 이상 없습니다.

서버에서 SHAPE 및 COORDS 속성을 해석하고 변경할 수 있습니다(이 릴리스에서는 SHAPE=CIRCLE이 지원되지 않음). `<AREA>`의 다른 모든 특성은 수정 없이 전달됩니다. COORDS 속성으로 지정된 좌표 값은 수정되지 않은 소스 이미지의 왼쪽 상단 모서리에서 픽셀 오프셋이어야 합니다. (`%` 좌표는 이 릴리스에서 지원되지 않으므로 올바르게 처리되지 않을 수 있습니다.)

## 속성 {#section-f52d89fd399b4356ac05277e6c12f956}

텍스트 문자열 값입니다. 지정하면 하나 이상의 완전한 HTML `<AREA>` 요소여야 합니다.

이 필드는 텍스트 문자열 현지화에 적용됩니다. 자세한 내용은 *HTTP 프로토콜 참조*&#x200B;의 [텍스트 문자열 지역화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)를 참조하십시오.

## 기본값 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

없음.

## 참조 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[맵=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [텍스트 문자열 로컬라이제이션](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
