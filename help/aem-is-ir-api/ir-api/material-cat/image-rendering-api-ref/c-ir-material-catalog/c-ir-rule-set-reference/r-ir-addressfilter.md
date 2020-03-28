---
description: 주소 필터 요소입니다. <rule> 요소의 선택 사항입니다. 규칙이 적용될 때 ClientAddressFilter 속성을 무시합니다.
seo-description: 주소 필터 요소입니다. <rule> 요소의 선택 사항입니다. 규칙이 적용될 때 ClientAddressFilter 속성을 무시합니다.
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# addressfilter{#addressfilter}

주소 필터 요소입니다. 선택 `<rule>` 사항입니다. 규칙이 적용될 때 속성::ClientAddressFilter를 무시합니다.

## 속성 {#section-e7a0960f7f0045da91de37824aa4aeaa}

없음.

## 데이터 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

쉼표로 구분된 IP 주소 목록입니다. 각 개별 주소에는 선택 사항인 넷마스크 접미사를 포함하여 IP 주소 범위의 지정을 허용할 수 있습니다. 자세한 내용은 ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`를 참조하십시오.

## 설명 {#section-099b7839c4be40c68cbff29dad14e7d5}

이 이미지 카탈로그에 대한 액세스는 `<addressfilter>` 요소에 지정하여 하나 이상의 특정 IP 주소로 제한할 수 있습니다. 클라이언트 IP 주소가 일치하지 않는 경우 &quot;요청 거부&quot; 오류가 클라이언트에 반환됩니다.

비어 있거나 지정되지 않은 경우 액세스가 `<addressfilter>` 제한되지 않습니다.

요소의 `<expression>` 요소가 없거나 비어 있으면, 이 `<rule>` 요소는 모든 요청에 `<addressfilter>` 적용됩니다.

`localhost` 은 명시적으로 지정되지 않더라도 항상 `ClientAddressFilter` 정의의 일부분입니다. 사양의 요청에 `localhost` `ClientAddressFilter` 관계없이 발신 요청은 거부되지 않습니다.

## SeeAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[속성::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
