---
description: 클라이언트 IP 주소 필터. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

클라이언트 IP 주소 필터. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.

지정하면 목록에 없는 IP 주소의 클라이언트에서 가져온 이 이미지 카탈로그에 대한 요청이 거부됩니다.

## 속성 {#section-d785265988324af68835410c9ba54147}

선택 가능한 넷마스크가 있는 쉼표로 구분된 IP 주소 목록(CIDR 표기법 사용):

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> ddd.ddd.ddd.ddd</span> 형식의 IP 주소입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>넷 마스크(0...32). </p></td> 
 </tr> 
</table>

`<addressfilter>` 요소가 있는 전처리 규칙이 적용되면 이 특성은 무시됩니다.

## 기본값 {#section-de26e8c9225745e985e4beac1f03f4f6}

정의되지 않았거나 비어 있는 경우 `default::AddressFilter`에서 상속됩니다.

## 예제 {#section-a955314d2b6a4213a16c12a8b18d8627}

액세스 제한 없음: `0.0.0.0/0`

192: `192.0.0.0/8`(으)로 시작하는 모든 주소에 액세스 권한 부여

주소가 192.168.12.0에서 192.168.13.255 사이인 512개 호스트에 대한 액세스 권한 부여: `192.168.12.0/23`

단일 IP 주소 `192.168.2.117` 또는 `192.168.2.117/32`에 대한 액세스 권한 부여

## 참조 {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
