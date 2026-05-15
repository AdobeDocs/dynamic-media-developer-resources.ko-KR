---
description: 이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스인 서버 관리자에 의해 관리됩니다(S7Supervisor.exe, 서비스 Campaign 컨트롤 패널에서 'Dynamic Media 이미지 제공'으로 나열됨).
solution: Experience Manager
title: 서버 감독자
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
TQID: 'https://experienceleague.adobe.com/D3cGGQLVly7MwWSvSjkWcWkuR9kVUFC9sSvItZm6eOc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# 서버 감독자{#server-supervisor}

이미지 제공 구성 요소는 Linux 데몬 또는 Windows 서비스인 서버 관리자에 의해 관리됩니다(S7Supervisor.exe, 서비스 Campaign 컨트롤 패널에서 &#39;Dynamic Media 이미지 제공&#39;으로 나열됨).

다른 이미지 제공 구성 요소를 시작 및 중지하는 것 외에도 서버 감독자는 이러한 다른 구성 요소의 상태를 확인할 책임이 있습니다. 구성 요소가 충돌하면 서비스 중단을 최소화하기 위해 자동으로 다시 시작됩니다.

## 시작 및 중지 {#section-061d28d74e034a30adc39ea3e2031cd0}

이미지 제공 유틸리티 스크립트를 사용하여 서버 감독자가 시작, 중지 및 다시 시작됩니다. 자세한 내용은 [유틸리티 설명서](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)를 참조하세요.

서버 감독자를 시작하고 중지하면 다른 모든 이미지 제공 구성 요소가 자동으로 시작되고 중지됩니다.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
