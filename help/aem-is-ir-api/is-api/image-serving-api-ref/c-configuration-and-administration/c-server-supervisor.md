---
description: 이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스(S7Supervisor.exe, 서비스 Campaign 컨트롤 패널에서 'Dynamic Media 이미지 제공'으로 나열됨)인 서버 감독자가 관리합니다.
solution: Experience Manager
title: 서버 감독자
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 서버 감독자{#server-supervisor}

이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스(S7Supervisor.exe, 서비스 Campaign 컨트롤 패널에서 &#39;Dynamic Media 이미지 제공&#39;으로 나열됨)인 서버 감독자가 관리합니다.

다른 이미지 제공 구성 요소를 시작 및 중지하는 것 외에도 서버 감독자는 이러한 다른 구성 요소의 상태를 보장할 책임이 있습니다. 구성 요소가 충돌하는 경우 서비스 중단을 최소화하기 위해 자동으로 다시 시작됩니다.

## 시작 및 중지 {#section-061d28d74e034a30adc39ea3e2031cd0}

Server Supervisor가 Image Serving 유틸리티 스크립트를 사용하여 시작, 중지 및 다시 시작됩니다. 자세한 내용은 [유틸리티 설명서](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)를 참조하십시오.

서버 수퍼바이저가 자동으로 시작되고 중지되면 다른 모든 이미지 제공 구성 요소가 자동으로 시작되고 중지됩니다.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
