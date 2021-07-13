---
description: 주소 필터 요소입니다. <규칙> 요소에서 선택 사항입니다. 규칙이 적용될 때 ClientAddressFilter 특성을 무시합니다.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 4%

---

# addressfilter{#addressfilter}

주소 필터 요소입니다. `<rule>` 요소에서 선택 사항입니다. 규칙이 적용될 때 특성::ClientAddressFilter를 무시합니다.

## 속성 {#section-e7a0960f7f0045da91de37824aa4aeaa}

없음.

## 데이터 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

쉼표로 구분된 IP 주소 목록. 각 개별 주소에는 IP 주소 범위를 지정할 수 있도록 선택적 netmask 접미사가 포함될 수 있습니다. 자세한 내용은 ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`를 참조하십시오.

## 설명 {#section-099b7839c4be40c68cbff29dad14e7d5}

이 이미지 카탈로그에 대한 액세스는 `<addressfilter>` 요소에 지정하여 하나 이상의 특정 IP 주소로 제한할 수 있습니다. 클라이언트 IP 주소가 일치하지 않는 경우 &quot;요청 거부&quot; 오류가 클라이언트에 반환됩니다.

`<addressfilter>`이 비어 있거나 지정되지 않은 경우 액세스가 제한되지 않습니다.

`<rule>` 요소의 `<expression>`이 없거나 비어 있으면 `<addressfilter>`가 모든 요청에 적용됩니다.

`localhost` 는 명시적으로 지정하지  `ClientAddressFilter` 않더라도 항상 정의의 일부입니다. `ClientAddressFilter` 사양에 관계없이 `localhost`에서 시작된 요청은 거부되지 않습니다.

## SaaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
