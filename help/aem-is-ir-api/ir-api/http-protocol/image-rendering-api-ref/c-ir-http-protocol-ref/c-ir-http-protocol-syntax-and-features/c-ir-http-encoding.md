---
title: 이미지 렌더링 HTTP 인코딩
description: 명령 값은 %xx 이스케이프 시퀀스를 사용하여 http 인코딩해야 하므로 값 문자열에 예약된 문자 '=', '&' 및 '%'가 포함되지 않습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# 이미지 렌더링 HTTP 인코딩{#image-rendering-http-encoding}

명령 값은 %xx 이스케이프 시퀀스를 사용하여 http 인코딩해야 하므로 값 문자열에 예약된 문자 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;가 포함되지 않습니다.

그렇지 않으면 표준 HTTP 인코딩 규칙이 적용됩니다. HTTP 사양에 &#39; &#39; &#39;(space), &#39;&quot;&#39;(큰따옴표), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; 및 &#39;>&#39;와 같은 안전하지 않은 문자와 `<return>` 및 `<tab>`과(와) 같은 모든 제어 문자의 인코딩이 필요합니다.

**주의:** 요청 중첩 구분 기호로 사용되는 중괄호 { }은(는) 인코딩할 수 없습니다. 일부 이메일 클라이언트는 포함된 HTTP 요청에서 중괄호를 인코딩합니다. 이 문제가 발생하면 이미지 렌더링에서 중괄호 대신 괄호( )를 사용할 수 있습니다.

## 예 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

위의 요청 조각은 다음과 같이 인코딩해야 합니다.

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 참조 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1 사양(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
