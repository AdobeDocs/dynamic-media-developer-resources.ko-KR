---
description: 지정된 회사의 활성 게시 컨텍스트 목록을 가져옵니다. 게시 컨텍스트는 컨텍스트에 대해 정의된 활성 서버가 하나 이상 있는 경우 활성 상태로 간주됩니다.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 11%

---

# getActivePublishContext{#getactivepublishcontext}

지정된 회사의 활성 게시 컨텍스트 목록을 가져옵니다. 게시 컨텍스트는 컨텍스트에 대해 정의된 활성 서버가 하나 이상 있는 경우 활성 상태로 간주됩니다.

구문

## 승인된 사용자 유형 {#section-eb22397744434dfe92a59ffa2883c2e7}

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
| company핸들 | `xsd:string` | 예 | 활성 게시 컨텍스트를 쿼리하기 위한 회사의 핸들입니다. |

**출력(getActivePublishContextsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| contextArray | `types:StringArray` | 예 | Publish 컨텍스트에서 0개 이상의 값을 포함할 수 있는 활성 게시 컨텍스트의 배열입니다. |
