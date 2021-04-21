---
description: 내부 용도로만 사용하십시오. 사용자는 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 14%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

내부 용도로만 사용하십시오. 사용자는 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.

구문

## 인증된 사용자 유형 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-79f0d54acd604ad2a5c96679334f2424}

**입력(getImageServingPublishSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 제작 설정을 제공하는 이미지가 있는 회사에 대한 핸들입니다. |
| `*`contextHandle`*` | `xsd:string` | 예 | 게시 컨텍스트를 처리합니다. |

**출력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | 예 | 이미지 서버 제작 설정의 배열입니다. |

