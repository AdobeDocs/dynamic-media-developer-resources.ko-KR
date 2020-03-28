---
description: 명령 값은 %xx 이스케이프 시퀀스를 사용하여 http 인코딩되어야 합니다. 따라서 값 문자열에 예약된 문자 '=', '&' 및 '%'가 포함되지 않습니다.
seo-description: 명령 값은 %xx 이스케이프 시퀀스를 사용하여 http 인코딩되어야 합니다. 따라서 값 문자열에 예약된 문자 '=', '&' 및 '%'가 포함되지 않습니다.
seo-title: 이미지 렌더링 HTTP 인코딩
solution: Experience Manager
title: 이미지 렌더링 HTTP 인코딩
topic: Scene7 Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 이미지 렌더링 HTTP 인코딩{#image-rendering-http-encoding}

명령 값은 %xx 이스케이프 시퀀스를 사용하여 http 인코딩되어야 합니다. 따라서 값 문자열에 예약된 문자 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;가 포함되지 않습니다.

그렇지 않으면 표준 HTTP 인코딩 규칙이 적용됩니다. HTTP 사양은 &#39;(공백), &#39;&quot;(큰따옴표), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39;, &#39;>&#39; 등의 안전하지 않은 문자뿐만 아니라 `<return>` 및 `<tab>`같은 모든 컨트롤 문자를 인코딩해야 합니다.

**주의:** 요청 중첩 구분 기호로 사용되는 중괄호 {}는 인코딩되지 않아야 합니다. 일부 이메일 클라이언트는 임베드된 HTTP 요청에 중괄호를 불행히도 인코딩합니다. 문제가 있는 경우 이미지 렌더링에서는 중괄호 대신 괄호()를 사용할 수 있습니다.

## 예 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

위의 요청 조각은 다음과 같이 인코딩되어야 합니다.

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 참조 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1 사양(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
