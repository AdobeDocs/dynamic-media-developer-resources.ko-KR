---
description: 이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스(서비스 제어판에서 'Scene7 이미지 제공'으로 나열된 S7Supervisor.exe)인 서버 수퍼바이저가 관리합니다.
seo-description: 이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스(서비스 제어판에서 'Scene7 이미지 제공'으로 나열된 S7Supervisor.exe)인 서버 수퍼바이저가 관리합니다.
seo-title: 서버 관리자
solution: Experience Manager
title: 서버 관리자
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 서버 관리자{#server-supervisor}

이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스(서비스 제어판에서 &#39;Scene7 이미지 제공&#39;으로 나열된 S7Supervisor.exe)인 서버 수퍼바이저가 관리합니다.

다른 이미지 제공 구성 요소를 시작 및 중지하는 것 외에도 서버 감독자는 이러한 다른 구성 요소의 상태를 보장할 책임이 있습니다. 구성 요소가 충돌하는 경우 서비스 중단을 최소화하도록 자동으로 다시 시작됩니다.

## 시작 및 중지 {#section-061d28d74e034a30adc39ea3e2031cd0}

Server Supervisor가 이미지 제공 유틸리티 스크립트로 시작, 중지 및 다시 시작됩니다. See the [Utilities documentation](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) for more information.

서버 수퍼바이저를 시작 및 중지하면 다른 모든 이미지 제공 구성 요소가 자동으로 시작되고 중지됩니다.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
