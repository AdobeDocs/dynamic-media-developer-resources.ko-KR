---
title: 이미지 렌더링 HTTP 인코딩
description: 값 문자열에 예약된 문자 '=', '&' 및 '%'가 포함되지 않도록 %xx 이스케이프 시퀀스를 사용하여 명령 값을 http로 인코딩해야 합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# 이미지 렌더링 HTTP 인코딩{#image-rendering-http-encoding}

값 문자열에 예약된 문자 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;가 포함되지 않도록 %xx 이스케이프 시퀀스를 사용하여 명령 값을 http로 인코딩해야 합니다.

그렇지 않으면 표준 HTTP 인코딩 규칙이 적용됩니다. HTTP 사양은 &#39;(space), &#39;&quot;(큰따옴표), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39;, &#39;>&#39; 등의 안전하지 않은 문자와 같은 컨트롤 문자를 인코딩해야 합니다. `<return>` 및 `<tab>`.

**주의:** 요청 중첩 구분 기호로 사용된 중괄호 { }는 인코딩할 수 없습니다. 특정 이메일 클라이언트는 안타깝게도 포함된 HTTP 요청에 중괄호를 인코딩합니다. 문제가 되는 경우 이미지 렌더링에서는 중괄호 대신 괄호( )를 사용할 수 있습니다.

## 예 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

위의 요청 조각을 다음과 같이 인코딩해야 합니다.

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 참조 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1 사양(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
