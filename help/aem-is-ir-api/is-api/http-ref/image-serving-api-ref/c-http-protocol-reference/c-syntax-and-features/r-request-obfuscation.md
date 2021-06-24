---
description: 표준 base64 인코딩을 적용하여 선택적 잠금 접미사를 포함하여 요청 문자열의 전체 수정자 부분의 내용을 가려낼 수 있습니다.
solution: Experience Manager
title: 난독화 요청
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# 난독화 요청{#request-obfuscation}

표준 base64 인코딩을 적용하여 선택적 잠금 접미사를 포함하여 요청 문자열의 전체 수정자 부분의 내용을 가려낼 수 있습니다.

`attribute::RequestObfuscation` 이 설정된 경우 서버가 디코딩을 시도합니다. 디코딩이 실패하면 요청이 거부됩니다. 요청 잠금 및 요청 난독화가 모두 적용되는 경우, 잠금 접미사를 생성하여 base64 인코딩 앞에 추가해야 합니다.

>[!IMPORTANT]
>
>이 기능을 활성화하면 <br>- Dynamic Media 사용자 인터페이스에 **[!UICONTROL 마지막으로 게시된]** 필드에 대한 올바른 세부 정보가 표시되지 않을 수 있는 사용 제한 사항이 있음을 알아두십시오. 그러나 게시에는 영향을 주지 않습니다.<br>- 현재, 난독화 요청 및 **[!UICONTROL 요청 위치가]** 활성화되어 있으면 HLS  **[!UICONTROL 비디오 스트리밍]** 이 작동하지 않습니다.<br>- 현재, 일부 Dynamic Media 뷰어는  **[!UICONTROL 난독화 요청]** 및  **[!UICONTROL 요청 위치가]** 활성화되어 있을 때 작동하지 않습니다.

## 예 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

코드를 다음과 같이 추가합니다.

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

요청을 난독화하려면 값 문자열에서 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;의 모든 항목을 &#39;%xx&#39; 인코딩을 사용하여 이스케이프해야 합니다. Base64 인코딩은 http 전송에 안전하므로 요청 잠금이 적용되더라도 난독화 전 또는 후에 요청의 *수정자* 부분을 http로 인코딩할 필요가 없습니다.

## 참조 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP 인코딩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [요청 잠금](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c),  [속성::RequestObfusation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
