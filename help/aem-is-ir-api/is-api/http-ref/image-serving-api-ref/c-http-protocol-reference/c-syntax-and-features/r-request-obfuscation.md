---
description: 선택적 잠금 접미사를 포함한 요청 문자열의 전체 수정자 부분의 내용은 표준 base64 인코딩을 적용하여 숨길 수 있습니다.
solution: Experience Manager
title: 난독화 요청
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# 난독화 요청{#request-obfuscation}

선택적 잠금 접미사를 포함한 요청 문자열의 전체 수정자 부분의 내용은 표준 base64 인코딩을 적용하여 숨길 수 있습니다.

`attribute::RequestObfuscation`이(가) 설정된 경우 서버에서 디코딩하려고 합니다. 디코딩에 실패하면 요청이 거부됩니다. 요청 잠금 및 요청 난독화가 모두 적용되는 경우 base64 인코딩 전에 잠금 접미사를 생성하고 추가해야 합니다.

>[!IMPORTANT]
>
>이 기능을 사용하는 경우 <br>을(를) 포함하는 특정 사용 제한 사항이 있습니다. Dynamic Media 사용자 인터페이스에 **[!UICONTROL 마지막으로 게시됨]** 필드에 대한 올바른 세부 정보가 표시되지 않을 수 있습니다. 그러나 이 영향은 게시에 영향을 주지 않습니다.<br>- 현재 **[!UICONTROL 난독화 요청]** 및 **[!UICONTROL 잠금 요청]**&#x200B;을 사용하면 HLS 비디오 스트리밍이 작동하지 않습니다.<br>- 현재 **[!UICONTROL 난독화 요청]** 및 **[!UICONTROL 잠금 요청]**&#x200B;을 사용하도록 설정한 경우 일부 Dynamic Media 뷰어가 작동하지 않습니다.

## 예 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

다음을 인코딩합니다.

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

값 문자열에서 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;는 요청이 난독화되기 전에 &#39;%xx&#39; 인코딩을 사용하여 이스케이프해야 합니다. base64 인코딩은 http 전송에 안전하므로 난독화 전이나 후에 요청의 *modifiers* 부분을 http 인코딩할 필요가 없습니다.

## 참조 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP 인코딩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [잠금 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [특성::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
