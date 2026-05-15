---
title: 트러스트된 도메인
description: Flash 애플리케이션 웹 도메인. Adobe Flash 응용 프로그램에서는 swf 형식으로 제공된 이미지의 속성에 액세스해야 할 수 있습니다. swf는 신뢰할 수 있는 응용 프로그램 도메인의 이름을 등록하여 액세스 권한을 명시적으로 부여해야 합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
TQID: 'https://experienceleague.adobe.com/GgLL3XL2Km0RvlfK3fjeD95FkgzO9OEcxNyyTZ8Y738'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 2%

---

# 트러스트된 도메인{#trusteddomains}

Flash 애플리케이션 웹 도메인. Adobe Flash 응용 프로그램에서는 swf 형식으로 제공된 이미지의 속성에 액세스해야 할 수 있습니다. swf는 신뢰할 수 있는 응용 프로그램 도메인의 이름을 등록하여 액세스 권한을 명시적으로 부여해야 합니다.

## 속성 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

웹 도메인 이름의 쉼표로 구분된 목록이 포함된 문자열입니다. 비어 있는 경우 [!DNL swf] 형식의 응답에서 이미지 속성에 액세스할 수 있으려면 이미지 렌더링과 동일한 도메인에서 응용 프로그램을 제공해야 합니다.

## 기본값 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

없는 경우 `default::TrustedDomains`에서 상속됨.

## 참조 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [특성::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
