---
description: 내부 용도로만 사용하십시오. 이미지 렌더링 재료 카탈로그 참조 카탈로그 속성 섹션을 참조하십시오.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 16%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

내부 용도로만 사용하십시오. 이미지 렌더링 재료 카탈로그 참조 카탈로그 속성 섹션을 참조하십시오.

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
| `*`companyHandle`*` | `xsd:string` | 예 | 가져오려는 이미지 렌더링 게시 설정이 있는 회사에 대한 핸들입니다. |
| `*`contextHandle`*` | `xsd:string` | 예 | 게시 컨텍스트를 처리합니다. |

**출력(getImageRenderingPublishSettingsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | 예 | 이미지 렌더링 게시 설정. |

