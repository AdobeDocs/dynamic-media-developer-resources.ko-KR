---
description: 주소 필터 요소를 참조하십시오. <rule> 및 <pathrule> 요소의 선택 사항입니다.
seo-description: 주소 필터 요소를 참조하십시오. <rule> 및 <pathrule> 요소의 선택 사항입니다.
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---


# addressfilter{#addressfilter}

주소 필터 요소를 참조하십시오. `<rule>` 및 `<pathrule>` 요소의 선택 사항입니다.

규칙이 적용될 때 `attribute::ClientAddressFilter`을(를) 무시합니다.

## 속성 {#section-31e9ad29e9934933ac154bccbc729172}

없음.

## 데이터 {#section-c762bdfe425140d689ea5abf25e9a48a}

쉼표로 구분된 IP 주소 목록. 각 개별 주소에는 IP 주소 범위를 지정할 수 있도록 선택적 netmask 접미사를 포함할 수 있습니다. 자세한 내용은 `attribute::ClientAddressFilter`를 참조하십시오.

## 설명 {#section-d561b2485e004ef8a2085997d0f4bca6}

이 이미지 카탈로그에 대한 액세스는 `<addressfilter>` 요소에 지정하여 하나 이상의 특정 클라이언트 IP 주소로 제한할 수 있습니다. 클라이언트 IP 주소가 일치하지 않는 경우 &quot;요청이 거부됨&quot; 오류가 클라이언트에 반환됩니다.

`<addressfilter>`이(가) 비어 있거나 지정되지 않은 경우 액세스가 제한되지 않습니다.

`<rule>` 요소의 `<expression>`이 없거나 비어 있으면 `<addressfilter>`가 모든 요청에 적용됩니다.

## 참조 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[특성::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
