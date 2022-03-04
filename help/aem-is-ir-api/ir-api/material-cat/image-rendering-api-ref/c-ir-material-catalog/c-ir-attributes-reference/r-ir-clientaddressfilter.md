---
description: 클라이언트 IP 주소 필터입니다. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

클라이언트 IP 주소 필터입니다. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.

이 옵션을 지정하면 목록에 없는 IP 주소의 클라이언트에서 가져온 이 이미지 카탈로그에 대한 요청이 거부됩니다. `localhost` 는 항상 암시적으로 `ClientAddressFilter` 명시적으로 지정하지 않더라도 정의. 보낸 요청 `localhost` 에 관계 없이 거부되지 않습니다 `ClientAddressFilter` 사양.

## 속성 {#section-21a2992f108d42fb8660c0d65aa61e13}

넷마스크(옵션)가 있는 쉼표로 구분된 IP 주소 목록([CIDR 표기법](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) 이 사용됨):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 의 IP 주소 *[!DNL ddd.ddd.ddd.ddd]* 포맷

* *[!DNL netmask]* 네트 마스크(0...32)

이 속성은 `<addressfilter>` 요소가 적용됩니다.

## 기본값 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

상속됨 `default::AddressFilter` 정의되지 않았거나 비어 있는 경우.

## 예제 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 액세스 제한 없음: `0.0.0.0/0`
* 다음으로 시작하는 모든 주소에 대한 액세스 권한 부여 `192: 192.0.0.0/8`
* 다음 사이의 주소가 있는 512 호스트에 대한 액세스 권한 부여 `192.168.12.0` 및 `192.168.13.255: 192.168.12.0/23`

* 단일 IP 주소에 대한 액세스 권한 부여: `192.168.2.117` 또는 `192.168.2.117/32`

## 참조 {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
