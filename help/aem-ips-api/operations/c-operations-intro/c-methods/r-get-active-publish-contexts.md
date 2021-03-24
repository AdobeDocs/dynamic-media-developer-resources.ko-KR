---
description: 지정된 회사에 대한 활성 게시 컨텍스트 목록을 가져옵니다. 컨텍스트에 대해 하나 이상의 활성 서버가 정의된 경우 게시 컨텍스트는 활성으로 간주됩니다.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 10%

---


# getActivePublishContext{#getactivepublishcontext}

지정된 회사에 대한 활성 게시 컨텍스트 목록을 가져옵니다. 컨텍스트에 대해 하나 이상의 활성 서버가 정의된 경우 게시 컨텍스트는 활성으로 간주됩니다.

구문

## 인증된 사용자 유형 {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-a4be4024e55c472fa6728faec9c5e048}

**입력(getActivePublishContextsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 활성 게시 컨텍스트를 쿼리할 회사에 대한 핸들 |

**출력(getActivePublishContextsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | 예 | 게시 컨텍스트의 값이 0개 이상 포함될 수 있는 활성 게시 컨텍스트의 배열입니다. |

