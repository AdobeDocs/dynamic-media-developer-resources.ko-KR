---
description: 요청사항을 조작할 기회를 저감시키기 위해 간단한 잠금시설을 설치한다.
solution: Experience Manager
title: 잠금 요청
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
TQID: 'https://experienceleague.adobe.com/9icGIK7meNSVUzYnsFBFM-GwG7KLe90bMDuqN89xmMk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 0%

---

# 잠금 요청{#request-locking}

요청사항을 조작할 기회를 저감시키기 위해 간단한 잠금시설을 설치한다.

attribute::RequestLock이 설정된 경우 `&xxxx` 형식으로 잠금 값을 요청에 추가해야 합니다. xxxx는 4자리 16진수 값입니다. 이 16진수 값은 요청의 *수정자* 부분에 적용된 간단한 해싱 알고리즘을 사용하여 생성됩니다(*수정자*&#x200B;에서 URL 경로를 구분하는 &#39;?&#39; 뒤). 이 작업은 요청이 완전히 http 인코딩이 된 후에 수행해야 하지만 선택적으로 난독화되기 전에 수행해야 합니다. 요청을 난독화한 후 서버는 수정자 문자열에서 동일한 해싱 알고리즘을 사용합니다(잠금 값이 포함된 마지막 5자 제외). 생성된 키가 잠금과 일치하지 않으면 요청이 거부됩니다.

>[!IMPORTANT]
>
>이 기능을 사용하는 경우 <br>- Dynamic Media 사용자 인터페이스에 **[!UICONTROL 마지막으로 게시됨]** 필드에 대한 올바른 세부 정보가 표시되지 않을 수 있습니다. 그러나 이 효과는 게시에 영향을 주지 않습니다.<br>- 현재 **[!UICONTROL 난독화 요청]** 및 **[!UICONTROL 잠금 요청]**&#x200B;이 활성화되어 있으면 HLS 비디오 스트리밍이 작동하지 않습니다.<br>- 현재 **[!UICONTROL 난독화 요청]** 및 **[!UICONTROL 잠금 요청]**&#x200B;이 활성화되어 있으면 일부 Dynamic Media Viewer가 작동하지 않습니다.

C++ 요청 잠금 값을 생성하는 샘플 코드:

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

[HTTP 인코딩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [난독화 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [특성::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
