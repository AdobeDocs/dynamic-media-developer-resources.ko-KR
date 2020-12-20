---
description: 내부 용도로만 사용하십시오. 사용자는 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.
seo-description: 내부 용도로만 사용하십시오. 사용자는 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Scene7 Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 제작 설정을 제공하는 이미지가 있는 회사에 대한 핸들입니다. |
| ` *`contextHandle`*` | `xsd:string` | 예 | 게시 컨텍스트를 처리합니다. |

**출력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`publishSettingArray`*` | `xsd:string` | 예 | 이미지 서버 제작 설정의 배열입니다. |

