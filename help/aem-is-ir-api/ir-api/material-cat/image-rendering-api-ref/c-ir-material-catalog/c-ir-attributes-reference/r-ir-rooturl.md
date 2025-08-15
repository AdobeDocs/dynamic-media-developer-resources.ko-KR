---
title: RootUrl
description: 상대 이미지 URL의 루트 URL입니다. 상대 이미지 URL의 루트 URL을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# RootUrl{#rooturl}

상대 이미지 URL의 루트 URL입니다. 상대 이미지 URL의 루트 URL을 지정합니다. `attribute::RootUrl` 값이 `attribute::RootPath`(으)로 둘러싸인 경우 `src=` 대신 {curly braces}이(가) 사용됩니다.

## 속성 {#section-69cd0f71ea614770a8778c745d23197a}

텍스트 문자열 값입니다. 선행 프로토콜 식별자를 포함하는 절대 URL 루트 경로입니다. 지원되는 프로토콜은 HTTP, HTTPS 및 FTP입니다.

## 기본값 {#section-7a81569728474725a70f3a2cc4d48e85}

정의되지 않은 경우 `default::RootUrl`에서 상속됩니다. 정의되어 있지만 비어 있는 경우 상대 URL은 이 재질 카탈로그에서 지원되지 않습니다.

## 참조 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [특성:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
