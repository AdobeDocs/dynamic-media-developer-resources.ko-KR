---
description: SWF 뷰어 구성 설정을 업데이트합니다.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,뷰어 사전 설정
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 13%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

SWF 뷰어 구성 설정을 업데이트합니다.

구문

## 인증된 사용자 유형 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-29790d933fb24aa392d0cb2d52d1310f}

**입력(updateViewerConfigSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사를 담당합니다. |
| `*`assetHandle`*` | `xsd:string` | 예 | 자산 핸들. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 예 | 뷰어에 적용할 구성 설정의 배열입니다. |

**출력(updateViewerConfigSettingsReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.
