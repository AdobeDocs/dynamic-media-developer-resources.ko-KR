---
description: Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램은 fmt=swf 또는 fmt=swf3로 전달되는 이미지의 속성에 액세스해야 할 수 있습니다.
seo-description: Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램은 fmt=swf 또는 fmt=swf3로 전달되는 이미지의 속성에 액세스해야 할 수 있습니다.
seo-title: 트러스트된 도메인
solution: Experience Manager
title: 트러스트된 도메인
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# 트러스트된 도메인{#trusteddomains}

Flash 응용 프로그램 웹 도메인. Adobe Flash 응용 프로그램은 fmt=swf 또는 fmt=swf3로 전달되는 이미지의 속성에 액세스해야 할 수 있습니다.

swf는 신뢰하는 응용 프로그램 도메인의 이름을 등록하여 명시적으로 액세스 권한을 부여해야 합니다.

## 속성 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

웹 도메인 이름의 쉼표로 구분된 목록을 포함하는 문자열. 비어 있는 경우 swf 형식의 응답으로 이미지 속성에 액세스할 수 있으려면 이미지 렌더링과 동일한 도메인에서 응용 프로그램을 제공해야 합니다.

## 기본값 {#section-5c52ed3c7310488380f5a6f9540bf981}

없는 경우 `default::TrustedDomains`에서 상속됩니다.

## 참조 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
