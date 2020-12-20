---
description: 값 문자열에 예약된 문자 '=', '&' 및 '%'가 포함되지 않도록 %xx 이스케이프 시퀀스를 사용하여 명령 값을 http로 인코딩해야 합니다.
seo-description: 값 문자열에 예약된 문자 '=', '&' 및 '%'가 포함되지 않도록 %xx 이스케이프 시퀀스를 사용하여 명령 값을 http로 인코딩해야 합니다.
seo-title: 이미지 렌더링 HTTP 인코딩
solution: Experience Manager
title: 이미지 렌더링 HTTP 인코딩
topic: Scene7 Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 이미지 렌더링 HTTP 인코딩{#image-rendering-http-encoding}

값 문자열에 예약된 문자 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;가 포함되지 않도록 %xx 이스케이프 시퀀스를 사용하여 명령 값을 http로 인코딩해야 합니다.

그렇지 않으면 표준 HTTP 인코딩 규칙이 적용됩니다. HTTP 사양은 &#39;(space), &#39;&quot;(큰따옴표), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; 및 &#39;>&#39;와 같은 안전하지 않은 문자뿐만 아니라 `<return>` 및 `<tab>`과 같은 모든 제어 문자를 인코딩해야 합니다.

**주의:** 요청 중첩 구분 기호로 사용된 중괄호 { }는 인코딩할 수 없습니다. 안타깝게도 특정 이메일 클라이언트는 포함된 HTTP 요청에서 중괄호를 인코딩합니다. 이 문제가 발생하면 이미지 렌더링에서는 중괄호 대신 괄호( )를 사용할 수 있습니다.

## 예 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

위의 요청 조각을 다음과 같이 인코딩해야 합니다.

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 참조 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1 사양(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
