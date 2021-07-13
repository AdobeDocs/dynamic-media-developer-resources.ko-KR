---
description: 클라이언트 IP 주소 필터입니다. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

클라이언트 IP 주소 필터입니다. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.

지정하면 목록에 없는 IP 주소로 클라이언트에서 보낸 이 이미지 카탈로그에 대한 요청이 거부됩니다. `localhost` 는 명시적으로 지정하지  `ClientAddressFilter` 않더라도 항상 정의의 일부입니다. `ClientAddressFilter` 사양에 관계없이 `localhost`에서 시작된 요청은 거부되지 않습니다.

## 속성 {#section-21a2992f108d42fb8660c0d65aa61e13}

선택적 넷마스크가 있는 IP 주소의 쉼표로 구분된 목록([CIDR 표기법](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)이 사용됨):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP 주소  *[!DNL ddd.ddd.ddd.ddd]* 형식

* *[!DNL netmask]* 네트 마스크(0...32)

이 속성은 `<addressfilter>` 요소가 있는 사전 처리 규칙이 적용될 때 무시됩니다.

## 기본값 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

정의되지 않았거나 비어 있는 경우 `default::AddressFilter`에서 상속됩니다.

## 예제 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 액세스 제한 없음: `0.0.0.0/0`
* `192: 192.0.0.0/8`으로 시작하는 모든 주소에 대한 액세스 권한 부여
* `192.168.12.0` 과 `192.168.13.255: 192.168.12.0/23` 사이의 주소가 있는 512 호스트에 대한 액세스 권한을 부여합니다

* 단일 IP 주소에 대한 액세스 권한 부여: `192.168.2.117` 또는 `192.168.2.117/32`

## 참조 {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
