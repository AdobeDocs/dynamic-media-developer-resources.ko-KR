---
description: 색상 프로파일 포함을 참조하십시오. 작업 중인 ICC 색상 프로파일 또는 icc=로 지정된 프로파일을 응답 이미지에 포함할지 여부를 지정합니다.
seo-description: 색상 프로파일 포함을 참조하십시오. 작업 중인 ICC 색상 프로파일 또는 icc=로 지정된 프로파일을 응답 이미지에 포함할지 여부를 지정합니다.
seo-title: iccEmbed
solution: Experience Manager
title: iccEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: ccd3fd2f-6f73-4725-a51a-9daf643d71af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# iccEmbed{#iccembed}

색상 프로파일 포함을 참조하십시오. 작업 중인 ICC 색상 프로파일 또는 icc=로 지정된 프로파일을 응답 이미지에 포함할지 여부를 지정합니다.

`iccEmbed=0|1`

## 속성 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

요청 속성을 참조하십시오. 임베드할 수 있는 프로파일이 없는 경우 무시됩니다.

## 기본값 {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`를 선택합니다. 출력 이미지 형식이 ICC 프로파일 임베딩을 지원하지 않는 경우 무시됩니다.

자세한 내용은 [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)을 참조하십시오.

## 참조 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[속성::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
