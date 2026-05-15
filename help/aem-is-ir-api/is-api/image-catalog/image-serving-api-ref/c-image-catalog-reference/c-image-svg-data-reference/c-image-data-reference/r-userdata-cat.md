---
description: 사용자 데이터. 서버는 req=userdata에 대한 응답으로 이 필드의 내용을 클라이언트에 반환합니다.
solution: Experience Manager
title: 사용자 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
TQID: 'https://experienceleague.adobe.com/9jhCw--mmCQ1-j1uNGFmfTEcnkNzxbKfXJtve5GugdA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 3%

---

# 사용자 데이터{#userdata}

사용자 데이터. 서버는 req=userdata에 대한 응답으로 이 필드의 내용을 클라이언트에 반환합니다.

## 속성 {#section-06f2002b77d54a64be07f12fff54ad13}

텍스트 문자열 값입니다. [속성 데이터](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 형식을 사용하는 것이 좋습니다. 속성 데이터 형식을 사용하지 않는 경우 텍스트 문자열에 &#39;=&#39; 문자를 사용할 수 없습니다.

확대/축소, 회전 및 브로셔 뷰어 클라이언트는 이 필드를 속성 데이터 형식을 사용한다고 가정합니다. 이러한 클라이언트는 뷰어 구성 및 사용자 지정에 이 필드를 사용합니다. 자세한 내용은 뷰어 설명서 를 참조하십시오.

이 필드는 텍스트 문자열 현지화에 적용됩니다. 자세한 내용은 *HTTP 프로토콜 참조*&#x200B;의 [텍스트 문자열 지역화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)를 참조하십시오.

## 기본값 {#section-7ee879762130467199745f2abc662f1e}

없음.

## 참조 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [텍스트 문자열 지역화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
