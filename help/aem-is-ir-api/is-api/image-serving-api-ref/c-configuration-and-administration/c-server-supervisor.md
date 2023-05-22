---
description: 이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스인 서버 관리자에 의해 관리됩니다(S7Supervisor.exe, 서비스 Campaign 컨트롤 패널에서 'Dynamic Media 이미지 제공'으로 나열됨).
solution: Experience Manager
title: 서버 감독자
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 서버 감독자{#server-supervisor}

이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스인 서버 관리자에 의해 관리됩니다(S7Supervisor.exe, 서비스 Campaign 컨트롤 패널에서 &#39;Dynamic Media 이미지 제공&#39;으로 나열됨).

다른 이미지 제공 구성 요소를 시작 및 중지하는 것 외에도 서버 감독자는 이러한 다른 구성 요소의 상태를 확인할 책임이 있습니다. 구성 요소가 충돌하면 서비스 중단을 최소화하기 위해 자동으로 다시 시작됩니다.

## 시작 및 중지 {#section-061d28d74e034a30adc39ea3e2031cd0}

이미지 제공 유틸리티 스크립트를 사용하여 서버 감독자가 시작, 중지 및 다시 시작됩니다. 다음을 참조하십시오. [유틸리티 설명서](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) 추가 정보.

서버 감독자를 시작하고 중지하면 다른 모든 이미지 제공 구성 요소가 자동으로 시작되고 중지됩니다.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
