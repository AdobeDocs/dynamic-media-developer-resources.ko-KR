---
description: 뷰어 구성 설정을 자산에 첨부합니다. 뷰어 사전 설정 또는 뷰어의 소스 에셋이 될 수 있습니다.
seo-description: 뷰어 구성 설정을 자산에 첨부합니다. 뷰어 사전 설정 또는 뷰어의 소스 에셋이 될 수 있습니다.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Scene7 Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 10%

---


# setViewerConfigSettings{#setviewerconfigsettings}

뷰어 구성 설정을 자산에 첨부합니다. 뷰어 사전 설정 또는 뷰어의 소스 에셋이 될 수 있습니다.

구문

## 인증된 사용자 유형 {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-bcc8c83cc84141e8b1341be9133e8511}

**입력(setViewerConfigSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 담당입니다. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 자산 핸들. |
| ` *`name`*` | `xsd:string` | 예 | 자산 이름. |
| ` *`type`*` | `xsd:string` | 예 | 뷰어 구성을 적용할 자산의 유형입니다. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | 예 | 자산에 적용된 `ConfigSettings` 배열.. |

**출력(setViewerConfigSettingsParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.
