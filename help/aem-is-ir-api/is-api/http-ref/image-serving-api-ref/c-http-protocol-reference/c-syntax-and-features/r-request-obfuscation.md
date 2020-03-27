---
description: 선택적 잠금 접미사를 포함하여 요청 문자열의 전체 수정자 내용은 표준 base64 인코딩을 적용하여 가려질 수 있습니다.
seo-description: 선택적 잠금 접미사를 포함하여 요청 문자열의 전체 수정자 내용은 표준 base64 인코딩을 적용하여 가려질 수 있습니다.
seo-title: 난독화 요청
solution: Experience Manager
title: 난독화 요청
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 난독화 요청{#request-obfuscation}

선택적 잠금 접미사를 포함하여 요청 문자열의 전체 수정자 내용은 표준 base64 인코딩을 적용하여 가려질 수 있습니다.

설정된 경우 서버가 디코딩을 시도합니다. `attribute::RequestObfuscation` 디코딩에 실패하면 요청이 거부됩니다. 요청 잠금과 요청 난독화가 모두 적용되는 경우 잠금 접미어를 생성하여 base64 인코딩 앞에 추가해야 합니다.

## 예 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

다음으로 코드 추가:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

요청이 난독화되기 전에 값 문자열에 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;의 모든 발생을 &#39;%xx&#39; 인코딩을 사용하여 이스케이프해야 합니다. base64 인코딩은 http 전송에 안전하므로, 난독화 전 또는 후 요청의 *수정자* 부분을 http-인코딩할 필요가 없습니다.

## 참조 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP 인코딩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [요청 잠금](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [속성::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
