---
description: Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램에서 fmt=swf 또는 fmt=swf3로 전달된 이미지의 속성에 액세스해야 할 수 있습니다.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# TrustedDomains{#trusteddomains}

Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램에서 fmt=swf 또는 fmt=swf3로 전달된 이미지의 속성에 액세스해야 할 수 있습니다.

swf는 신뢰할 수 있는 응용 프로그램 도메인의 이름을 등록하여 액세스 권한을 명시적으로 부여해야 합니다.

## 속성 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

웹 도메인 이름을 쉼표로 구분한 목록을 포함하는 문자열입니다. 비어 있는 경우 이미지 렌더링 과 동일한 도메인에서 응용 프로그램을 제공해야 swf 형식의 응답으로 이미지 속성에 액세스할 수 있습니다.

## 기본값 {#section-5c52ed3c7310488380f5a6f9540bf981}

없는 경우 `default::TrustedDomains`에서 상속됨.

## 참조 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
