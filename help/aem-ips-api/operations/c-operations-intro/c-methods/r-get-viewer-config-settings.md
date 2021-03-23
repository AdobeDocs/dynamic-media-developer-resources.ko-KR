---
description: 지정된 자산과 연결된 모든 뷰어 구성 설정을 가져옵니다.
seo-description: 지정된 자산과 연결된 모든 뷰어 구성 설정을 가져옵니다.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
feature: Dynamic Media Classic,SDK/API,뷰어 사전 설정
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 17%

---


# getViewerConfigSettings{#getviewerconfigsettings}

지정된 자산과 연결된 모든 뷰어 구성 설정을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**입력(getViewerConfigSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 담당입니다. |
| `*`assetHandle`*` | `xsd:string` | 예 | 자산을 처리합니다. |

**출력(getViewerConfigSettingsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`type`*` | `xsd:string` | 예 | 구성 설정이 적용되는 뷰어 유형입니다. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | 예 | 뷰어 구성 설정의 배열입니다. |

