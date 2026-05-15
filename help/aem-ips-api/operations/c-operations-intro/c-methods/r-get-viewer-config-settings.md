---
description: 지정된 자산과 연결된 모든 뷰어 구성 설정을 가져옵니다.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
TQID: 'https://experienceleague.adobe.com/GeSAS1EP7Q6EgsQltyC-TVnxS0zusuKxKs6QL8wfLWw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 22%

---

# getViewerConfigSettings{#getviewerconfigsettings}

지정된 자산과 연결된 모든 뷰어 구성 설정을 가져옵니다.

구문

## 승인된 사용자 유형 {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**입력(getViewerConfigSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| assetHandle | `xsd:string` | 예 | 자산을 처리합니다. |

**출력(getViewerConfigSettingsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 유형 | `xsd:string` | 예 | 구성 설정이 적용되는 뷰어 유형입니다. |
| configSettingsArray | `types:ConfigSettingsArray` | 예 | 뷰어 구성 설정 배열. |
