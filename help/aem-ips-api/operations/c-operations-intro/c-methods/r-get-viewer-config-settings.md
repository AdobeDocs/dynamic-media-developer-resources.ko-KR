---
description: 지정된 자산과 연결된 모든 뷰어 구성 설정을 가져옵니다.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 22%

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
| companyHandle | `xsd:string` | 예 | 회사를 담당합니다. |
| assetHandle | `xsd:string` | 예 | 자산을 처리합니다. |

**출력(getViewerConfigSettingsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 유형 | `xsd:string` | 예 | 구성 설정이 적용되는 뷰어 유형입니다. |
| configSettingsArray | `types:ConfigSettingsArray` | 예 | 뷰어 구성 설정의 배열입니다. |
