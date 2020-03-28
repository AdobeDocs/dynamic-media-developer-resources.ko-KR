---
description: 주소 필터 요소입니다. <rule> 및 <pathrule> 요소의 선택 사항입니다.
seo-description: 주소 필터 요소입니다. <rule> 및 <pathrule> 요소의 선택 사항입니다.
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# addressfilter{#addressfilter}

주소 필터 요소입니다. 인 `<rule>` 및 `<pathrule>` 요소 선택 사항.

규칙이 적용되면 `attribute::ClientAddressFilter` 무시합니다.

## 속성 {#section-31e9ad29e9934933ac154bccbc729172}

없음.

## 데이터 {#section-c762bdfe425140d689ea5abf25e9a48a}

쉼표로 구분된 IP 주소 목록입니다. 각 개별 주소에는 선택 사항인 넷마스크 접미사를 포함하여 IP 주소 범위의 지정을 허용할 수 있습니다. 자세한 내용은 `attribute::ClientAddressFilter`를 참조하십시오.

## 설명 {#section-d561b2485e004ef8a2085997d0f4bca6}

이 이미지 카탈로그에 대한 액세스는 `<addressfilter>` 요소에 지정하여 하나 이상의 특정 클라이언트 IP 주소로 제한할 수 있습니다. 클라이언트 IP 주소가 일치하지 않는 경우 &quot;요청 거부&quot; 오류가 클라이언트에 반환됩니다.

비어 있거나 지정되지 않은 경우 액세스가 `<addressfilter>` 제한되지 않습니다.

요소의 `<expression>` 요소가 없거나 비어 있으면, 이 `<rule>` 요소는 모든 요청에 `<addressfilter>` 적용됩니다.

## 참조 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[속성::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
