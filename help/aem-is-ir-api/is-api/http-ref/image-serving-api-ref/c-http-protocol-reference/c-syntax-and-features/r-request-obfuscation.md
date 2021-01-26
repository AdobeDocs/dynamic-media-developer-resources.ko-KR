---
description: 선택적 잠금 접미사를 포함하여 요청 문자열의 전체 수정자 부분은 표준 base64 인코딩을 적용하여 가려질 수 있습니다.
seo-description: 선택적 잠금 접미사를 포함하여 요청 문자열의 전체 수정자 부분은 표준 base64 인코딩을 적용하여 가려질 수 있습니다.
seo-title: 난독화 요청
solution: Experience Manager
title: 난독화 요청
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---


# 난독화 요청{#request-obfuscation}

선택적 잠금 접미사를 포함하여 요청 문자열의 전체 수정자 부분은 표준 base64 인코딩을 적용하여 가려질 수 있습니다.

서버는 `attribute::RequestObfuscation`이(가) 설정된 경우 디코딩을 시도합니다. 디코딩에 실패하면 요청이 거부됩니다. 요청 잠금과 요청 난독화가 모두 적용되는 경우 잠금 접미사를 생성하여 base64 인코딩 전에 추가해야 합니다.

>[!IMPORTANT]
>
>이 기능을 활성화하면 <br>- Dynamic Media 사용자 인터페이스에 **[!UICONTROL 마지막으로 게시된 항목]** 필드에 대한 정확한 세부 정보가 표시되지 않을 수 있습니다. 그러나 이는 게시에 영향을 주지 않습니다.<br>- 현재, 요청 난독화 및 요청 위치&#x200B;**[!UICONTROL 가 활성화된 경우 HLS]** 비디오  **[!UICONTROL 스트리밍이]** 작동하지 않습니다.<br>- 현재 일부 Dynamic Media 뷰어는 요청 난독화 및  **[!UICONTROL 요청]** 위치 **[!UICONTROL 가 활성화된]** 경우 작동하지 않습니다.

## 예 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

다음으로 코드 추가:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

요청이 난독화되기 전에 값 문자열에 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39; 항목이 &#39;%xx&#39; 인코딩을 사용하여 이스케이프해야 합니다. 기본 64 인코딩은 http 전송에 안전하므로 요청 잠금이 적용되더라도 난독화 전 또는 후 요청의 *수정자* 부분을 http로 인코딩할 필요가 없습니다.

## 참조 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP 인코딩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [요청 잠금](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c),  [특성::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
