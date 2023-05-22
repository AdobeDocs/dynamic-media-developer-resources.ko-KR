---
title: 트러스트된 도메인
description: Flash 애플리케이션 웹 도메인. Adobe Flash 응용 프로그램을 사용하려면 swf 형식으로 제공된 이미지의 속성에 액세스해야 할 수 있습니다. swf는 신뢰할 수 있는 응용 프로그램 도메인의 이름을 등록하여 액세스 권한을 명시적으로 부여해야 합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# 트러스트된 도메인{#trusteddomains}

Flash 애플리케이션 웹 도메인. Adobe Flash 응용 프로그램을 사용하려면 swf 형식으로 제공된 이미지의 속성에 액세스해야 할 수 있습니다. swf는 신뢰할 수 있는 응용 프로그램 도메인의 이름을 등록하여 액세스 권한을 명시적으로 부여해야 합니다.

## 속성 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

웹 도메인 이름의 쉼표로 구분된 목록이 포함된 문자열입니다. 비어 있는 경우 의 이미지 속성에 액세스할 수 있으려면 이미지 렌더링과 동일한 도메인에서 애플리케이션을 제공해야 합니다. [!DNL swf]형식이 지정된 응답입니다.

## 기본값 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

상속 위치 `default::TrustedDomains` 없는 경우.

## 참조 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
