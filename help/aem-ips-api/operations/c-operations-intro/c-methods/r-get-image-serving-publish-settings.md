---
description: 내부 전용입니다. 사용자는 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 16%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

내부 전용입니다. 사용자는 이미지 제공 이미지 카탈로그 참조 - 속성 참조 섹션을 참조해야 합니다.

구문

## 승인된 사용자 유형 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-79f0d54acd604ad2a5c96679334f2424}

**입력(getImageServingPublishSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 이미지 제공 게시 설정이 있는 회사에 대한 핸들입니다. |
| context핸들 | `xsd:string` | 예 | 게시 컨텍스트에 대한 핸들입니다. |

**출력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| publishSettingsArray | `xsd:string` | 예 | 이미지 서버 게시 설정의 배열입니다. |
