---
description: 포함 색상 프로필. 작업 ICC 색상 프로파일 또는 icc=로 지정된 프로파일을 회신 이미지에 포함할지 여부를 지정합니다.
solution: Experience Manager
title: iccEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: bc5637f6-5452-4bfb-bf30-def6f153f4ad
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# iccEmbed{#iccembed}

포함 색상 프로필. 작업 ICC 색상 프로파일 또는 icc=로 지정된 프로파일을 회신 이미지에 포함할지 여부를 지정합니다.

`iccEmbed=0|1`

## 속성 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

요청 속성입니다. 포함할 수 있는 프로필이 없으면 무시됩니다.

## 기본값 {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`출력 이미지에 ICC 프로파일을 포함하지 않는 경우 출력 이미지 형식이 ICC 프로파일 포함을 지원하지 않으면 무시됩니다.

자세한 내용은 [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 를 참조하십시오.

## 참조 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
