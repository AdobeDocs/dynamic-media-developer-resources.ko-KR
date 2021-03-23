---
description: 사용자 데이터. 서버는 req=userdata에 대한 응답으로 이 필드의 내용을 클라이언트에 반환합니다.
seo-description: 사용자 데이터. 서버는 req=userdata에 대한 응답으로 이 필드의 내용을 클라이언트에 반환합니다.
seo-title: 사용자 데이터
solution: Experience Manager
title: 사용자 데이터
uuid: cadc9f3c-c0ca-4c88-bc8a-97c28b439b01
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 9%

---


# 사용자 데이터{#userdata}

사용자 데이터. 서버는 req=userdata에 대한 응답으로 이 필드의 내용을 클라이언트에 반환합니다.

## 속성 {#section-06f2002b77d54a64be07f12fff54ad13}

텍스트 문자열 값입니다. [속성 데이터](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 서식을 사용하는 것이 좋습니다. 속성 데이터 서식을 사용하지 않는 경우 텍스트 문자열에 &#39;=&#39; 문자가 포함되면 안 됩니다.

확대/축소, 회전 및 브로셔 뷰어 클라이언트는 속성 데이터 형식을 사용하기 위해 이 필드를 사용합니다. 이러한 클라이언트는 뷰어 구성 및 사용자 지정에 이 필드를 사용합니다. 자세한 내용은 뷰어 설명서를 참조하십시오.

이 필드는 텍스트 문자열 현지화에 참여합니다. 자세한 내용은 *HTTP 프로토콜 참조*&#x200B;의 [텍스트 문자열 현지화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)를 참조하십시오.

## 기본값 {#section-7ee879762130467199745f2abc662f1e}

없음.

## 참조 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [텍스트 문자열 현지화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
