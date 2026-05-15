---
description: 내부 전용입니다. 사용자는 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
TQID: 'https://experienceleague.adobe.com/-VBxIs4EWFDesksSnU-DpN2pg-LJUN60OPhqjQVqAr8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 16%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

내부 전용입니다. 사용자는 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.

구문

## 승인된 사용자 유형 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-79f0d54acd604ad2a5c96679334f2424}

**입력(getImageServingPublishSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 이미지 제공 게시 설정이 있는 회사에 대한 핸들입니다. |
| context핸들 | `xsd:string` | 예 | 게시 컨텍스트에 대한 핸들입니다. |

**출력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| publishSettingsArray | `xsd:string` | 예 | 이미지 서버 게시 설정의 배열입니다. |
