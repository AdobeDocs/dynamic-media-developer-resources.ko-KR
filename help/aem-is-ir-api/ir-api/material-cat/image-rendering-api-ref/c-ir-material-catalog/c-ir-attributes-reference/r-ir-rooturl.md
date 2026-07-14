---
title: RootUrl
description: 상대 이미지 URL의 루트 URL입니다. 상대 이미지 URL의 루트 URL을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
TQID: 'https://experienceleague.adobe.com/1wKgvbd1t4HyDlz-CTDkp2gQuryBJYfMyDG7SmVgNwE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# RootUrl{#rooturl}

상대 이미지 URL의 루트 URL입니다. 상대 이미지 URL의 루트 URL을 지정합니다. `src=` 값이 {curly braces}(으)로 둘러싸인 경우 `attribute::RootPath` 대신 `attribute::RootUrl`이(가) 사용됩니다.

## 속성 {#section-69cd0f71ea614770a8778c745d23197a}

텍스트 문자열 값입니다. 선행 프로토콜 식별자를 포함하는 절대 URL 루트 경로입니다. 지원되는 프로토콜은 HTTP, HTTPS 및 FTP입니다.

## 기본값 {#section-7a81569728474725a70f3a2cc4d48e85}

정의되지 않은 경우 `default::RootUrl`에서 상속됩니다. 정의되어 있지만 비어 있는 경우 상대 URL은 이 재질 카탈로그에서 지원되지 않습니다.

## 참조 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [특성:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

