---
description: 클라이언트 IP 주소 필터입니다. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.
seo-description: 클라이언트 IP 주소 필터입니다. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---


# ClientAddressFilter{#clientaddressfilter}

클라이언트 IP 주소 필터입니다. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.

지정된 경우 목록에 없는 IP 주소의 클라이언트에서 가져온 이미지 카탈로그에 대한 요청이 거부됩니다.

## 속성 {#section-d785265988324af68835410c9ba54147}

선택적 넷마스크가 있는 IP 주소의 쉼표로 구분된 목록(CIDR 표기법이 사용됨):

`*`ipAddress`*` `[`/  *`netmask`*`]`*  `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> ddd.ddd.ddd.ddd</span> 형식의 IP 주소입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>네트 마스크(0...32). </p></td> 
 </tr> 
</table>

이 속성은 `<addressfilter>` 요소가 있는 사전 처리 규칙이 적용될 때 무시됩니다.

## 기본값 {#section-de26e8c9225745e985e4beac1f03f4f6}

정의되지 않았거나 비어 있는 경우 `default::AddressFilter`에서 상속됩니다.

## 예제 {#section-a955314d2b6a4213a16c12a8b18d8627}

액세스 제한 없음:`0.0.0.0/0`

192부터 모든 주소에 액세스 권한 부여:`192.0.0.0/8`

192.168.12.0~192.168.13.255 사이의 주소가 있는 512 호스트에 대한 액세스 권한을 부여합니다.`192.168.12.0/23`

단일 IP 주소에 대한 액세스 권한 부여:`192.168.2.117` 또는 `192.168.2.117/32`

## 참조 {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
