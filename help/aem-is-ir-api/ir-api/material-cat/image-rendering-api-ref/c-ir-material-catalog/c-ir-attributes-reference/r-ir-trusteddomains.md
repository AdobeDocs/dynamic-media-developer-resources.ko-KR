---
description: Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램은 swf 형식으로 제공되는 이미지의 속성에 액세스해야 할 수 있습니다.swf는 신뢰하는 응용 프로그램 도메인의 이름을 등록하여 명시적으로 액세스 권한을 부여해야 합니다.
seo-description: Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램은 swf 형식으로 제공되는 이미지의 속성에 액세스해야 할 수 있습니다.swf는 신뢰하는 응용 프로그램 도메인의 이름을 등록하여 명시적으로 액세스 권한을 부여해야 합니다.
seo-title: 트러스트된 도메인 *
solution: Experience Manager
title: 트러스트된 도메인 *
topic: Scene7 Image Serving - Image Rendering API
uuid: c50180b1-9af7-45f1-878f-59f41f9958ae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# TrustedDomains *{#trusteddomains}

Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램은 swf 형식으로 제공되는 이미지의 속성에 액세스해야 할 수 있습니다.swf는 신뢰하는 응용 프로그램 도메인의 이름을 등록하여 명시적으로 액세스 권한을 부여해야 합니다.

## 속성 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

웹 도메인 이름의 쉼표로 구분된 목록을 포함하는 문자열. 비어 있는 경우 [!DNL swf] 형식 응답의 이미지 속성에 액세스할 수 있으려면 이미지 렌더링과 동일한 도메인에서 애플리케이션을 제공해야 합니다.

## 기본값 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

없는 경우 `default::TrustedDomains`에서 상속됩니다.

## 참조 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [속성::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
