---
description: 요청을 변경할 수 있는 기회를 줄이기 위해 간단한 잠금 기능이 제공됩니다.
seo-description: 요청을 변경할 수 있는 기회를 줄이기 위해 간단한 잠금 기능이 제공됩니다.
seo-title: 요청 잠금
solution: Experience Manager
title: 요청 잠금
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 요청 잠금{#request-locking}

요청을 변경할 수 있는 기회를 줄이기 위해 간단한 잠금 기능이 제공됩니다.

attribute::RequestLock이 설정된 경우 잠금 값이 요청에 추가되어야 합니다(예: xxxx는 4자리 16 `&xxxx`진수 값). 이 16진수 값은 요청의 *수정자* 부분에 적용된 단순 해싱 알고리즘을 사용하여 생성됩니다(&#39;?&#39; 다음에 URL 경로를 *수정자와*&#x200B;구분합니다. 이 작업은 요청이 완전히 http로 인코딩된 후 수행되어야 하지만 (선택 사항) 난독화되기 전에 수행해야 합니다. 요청을 난독화하면 서버는 수정자 문자열에서 동일한 해싱 알고리즘을 사용합니다(잠금 값이 들어 있는 마지막 5자 제외). 생성된 키가 잠금과 일치하지 않으면 요청이 거부됩니다.

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

[HTTP 인코딩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [요청 난독화](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [속성::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
