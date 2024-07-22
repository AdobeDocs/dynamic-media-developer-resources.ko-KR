---
description: 뷰어 구성 설정을 자산에 연결합니다. 뷰어 사전 설정 또는 뷰어에 대한 소스 자산일 수 있습니다.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

---

# setViewerConfigSettings{#setviewerconfigsettings}

뷰어 구성 설정을 자산에 연결합니다. 뷰어 사전 설정 또는 뷰어에 대한 소스 자산일 수 있습니다.

구문

## 승인된 사용자 유형 {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-bcc8c83cc84141e8b1341be9133e8511}

**입력(setViewerConfigSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| assetHandle | `xsd:string` | 예 | 에셋 핸들. |
| name | `xsd:string` | 예 | 에셋 이름. |
| 유형 | `xsd:string` | 예 | 뷰어 구성을 적용할 에셋의 유형입니다. |
| configSettingArray | `types:ConfigSettingArray` | 예 | 자산에 적용된 `ConfigSettings`의 배열.. |

**출력(setViewerConfigSettingsParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.
