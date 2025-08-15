---
description: 주소 필터 요소입니다. <rule> 및 <pathrule> 요소에서 선택 사항입니다.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 5%

---

# addressfilter{#addressfilter}

주소 필터 요소입니다. `<rule>` 및 `<pathrule>` 요소에서 선택 사항입니다.

규칙이 적용되면 `attribute::ClientAddressFilter`을(를) 재정의합니다.

## 속성 {#section-31e9ad29e9934933ac154bccbc729172}

없음.

## 데이터 {#section-c762bdfe425140d689ea5abf25e9a48a}

쉼표로 구분된 IP 주소 목록입니다. 각각의 개별 주소는 IP 주소 범위의 사양을 허용하기 위해 선택적 넷마스크 접미사를 포함할 수 있다. 자세한 내용은 `attribute::ClientAddressFilter`를 참조하십시오.

## 설명 {#section-d561b2485e004ef8a2085997d0f4bca6}

`<addressfilter>` 요소에서 하나 이상의 특정 클라이언트 IP 주소를 지정하여 이 이미지 카탈로그에 대한 액세스를 제한할 수 있습니다. 클라이언트 IP 주소가 일치하지 않는 경우 &quot;요청 거부&quot; 오류가 클라이언트에 반환됩니다.

`<addressfilter>`이(가) 비어 있거나 지정되지 않은 경우 액세스가 제한되지 않습니다.

`<expression>` 요소의 `<rule>`이(가) 없거나 비어 있으면 `<addressfilter>`이(가) 모든 요청에 적용됩니다.

## 참조 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
