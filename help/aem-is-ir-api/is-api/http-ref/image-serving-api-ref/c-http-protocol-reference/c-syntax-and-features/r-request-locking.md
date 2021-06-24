---
description: 요청 조작 기회를 줄이기 위해 간단한 잠금 기능이 제공됩니다.
solution: Experience Manager
title: 요청 잠금
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 요청 잠금{#request-locking}

요청 조작 기회를 줄이기 위해 간단한 잠금 기능이 제공됩니다.

특성::RequestLock이 설정된 경우 요청에 잠금 값을 추가해야 합니다(예: `&xxxx`). xxxx는 4자리 16진수 값입니다. 이 16진수 값은 요청의 *수정자* 부분(&#39;?&#39; 다음에 적용되는 간단한 해싱 알고리즘을 사용하여 생성됩니다. URL 경로를 *수정자*)에서 분리합니다. 이 작업은 요청이 완전히 http로 인코딩된 후(선택 사항) 난독화되기 전에 수행해야 합니다. 요청을 난독화하면 서버에서 수정자 문자열에서 동일한 해싱 알고리즘을 사용합니다(잠금 값이 포함된 마지막 5자 제외). 생성된 키가 잠금과 일치하지 않으면 요청이 거부됩니다.

>[!IMPORTANT]
>
>이 기능을 활성화하면 <br>- Dynamic Media 사용자 인터페이스에 **[!UICONTROL 마지막으로 게시된]** 필드에 대한 올바른 세부 정보가 표시되지 않을 수 있는 사용 제한 사항이 있음을 알아두십시오. 그러나 게시에는 영향을 주지 않습니다.<br>- 현재, 난독화 요청 및 **[!UICONTROL 요청 위치가]** 활성화되어 있으면 HLS  **[!UICONTROL 비디오 스트리밍]** 이 작동하지 않습니다.<br>- 현재, 일부 Dynamic Media 뷰어는  **[!UICONTROL 난독화 요청]** 및  **[!UICONTROL 요청 위치가]** 활성화되어 있을 때 작동하지 않습니다.

요청 잠금 값을 생성하기 위한 C++ 샘플 코드:

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## 참조 {#section-a6d45406c0354669ac581793e4fa8436}

[HTTP 인코딩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [요청 난독화](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d),  [속성::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
