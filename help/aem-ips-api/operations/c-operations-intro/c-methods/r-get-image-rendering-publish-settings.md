---
description: 내부용입니다. 이미지 렌더링 자재 카탈로그 참조-카탈로그 속성 섹션을 참조하십시오.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 16%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

내부용입니다. 이미지 렌더링 자재 카탈로그 참조-카탈로그 속성 섹션을 참조하십시오.

구문

## 인증된 사용자 유형 {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-4f2cb8c589384816bb2525654ec49963}

**입력(getImageRenderingPublishSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 가져올 이미지 렌더링 게시 설정이 있는 회사의 핸들입니다. |
| `*`contextHandle`*` | `xsd:string` | 예 | 게시 컨텍스트를 처리합니다. |

**출력(getImageRenderingPublishSettingsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | 예 | 이미지 렌더링 게시 설정. |
