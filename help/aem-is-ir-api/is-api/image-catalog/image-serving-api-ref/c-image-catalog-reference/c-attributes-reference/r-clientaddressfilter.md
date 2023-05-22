---
description: 클라이언트 IP 주소 필터. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

클라이언트 IP 주소 필터. 하나 이상의 IP 주소 또는 주소 범위를 지정할 수 있습니다.

지정하면 목록에 없는 IP 주소의 클라이언트에서 가져온 이 이미지 카탈로그에 대한 요청이 거부됩니다.

## 속성 {#section-d785265988324af68835410c9ba54147}

선택 가능한 넷마스크가 있는 쉼표로 구분된 IP 주소 목록(CIDR 표기법 사용):

`*`ip 주소`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ip 주소</span> </p> </td> 
  <td class="stentry"> <p>의 IP 주소 <span class="varname"> ddd.ddd.ddd.ddd</span> 포맷. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 넷마스크</span> </p></td> 
  <td class="stentry"> <p>넷 마스크(0...32). </p></td> 
 </tr> 
</table>

이 속성은 가 있는 전처리 규칙에서 무시됩니다. `<addressfilter>` 요소가 적용됩니다.

## 기본값 {#section-de26e8c9225745e985e4beac1f03f4f6}

상속 위치 `default::AddressFilter` 정의되지 않은 경우 또는 비어 있는 경우.

## 예제 {#section-a955314d2b6a4213a16c12a8b18d8627}

액세스 제한 없음: `0.0.0.0/0`

192로 시작하는 모든 주소에 대한 액세스 권한 부여: `192.0.0.0/8`

192.168.12.0과 192.168.13.255 사이의 주소를 가진 512개 호스트에 액세스 권한 부여: `192.168.12.0/23`

단일 IP 주소에 대한 액세스 권한 부여: `192.168.2.117` 또는 `192.168.2.117/32`

## 참조 {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
