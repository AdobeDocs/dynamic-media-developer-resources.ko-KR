---
description: SWF 뷰어 구성 설정을 업데이트합니다.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
TQID: 'https://experienceleague.adobe.com/YcfK5U6MKvmV2ulOQ3s2sOOBsgASSeslCIrk87xLAv8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 15%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

SWF 뷰어 구성 설정을 업데이트합니다.

구문

## 승인된 사용자 유형 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-29790d933fb24aa392d0cb2d52d1310f}

**입력(updateViewerConfigSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| assetHandle | `xsd:string` | 예 | 에셋 핸들. |
| configSettingArray | `types:ConfigSettingArray` | 예 | 뷰어에 적용할 구성 설정의 배열입니다. |

**출력(updateViewerConfigSettingsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.
