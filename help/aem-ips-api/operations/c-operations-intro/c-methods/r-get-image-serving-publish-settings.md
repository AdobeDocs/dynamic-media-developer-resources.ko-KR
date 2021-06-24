---
description: 내부용입니다. 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

내부용입니다. 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.

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
| `*`companyHandle`*` | `xsd:string` | 예 | 이미지 제공 게시 설정이 있는 회사의 핸들입니다. |
| `*`contextHandle`*` | `xsd:string` | 예 | 게시 컨텍스트를 처리합니다. |

**출력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | 예 | 이미지 서버 게시 설정의 배열입니다. |
