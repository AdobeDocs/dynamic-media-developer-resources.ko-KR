---
description: Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램은 swf 형식으로 전달된 이미지의 속성에 액세스해야 할 수 있습니다. swf는 신뢰할 수 있는 응용 프로그램 도메인의 이름을 등록하여 액세스 권한을 명시적으로 부여해야 합니다.
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# TrustedDomains *{#trusteddomains}

Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램은 swf 형식으로 전달된 이미지의 속성에 액세스해야 할 수 있습니다. swf는 신뢰할 수 있는 응용 프로그램 도메인의 이름을 등록하여 액세스 권한을 명시적으로 부여해야 합니다.

## 속성 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

웹 도메인 이름을 쉼표로 구분한 목록을 포함하는 문자열입니다. 비어 있는 경우 [!DNL swf] 형식의 응답에서 이미지의 속성에 액세스할 수 있으려면 이미지 렌더링과 동일한 도메인에서 응용 프로그램을 제공해야 합니다.

## 기본값 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

없는 경우 `default::TrustedDomains`에서 상속됨.

## 참조 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
