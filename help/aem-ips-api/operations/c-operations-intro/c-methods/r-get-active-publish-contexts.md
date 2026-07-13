---
description: 지정된 회사의 활성 게시 컨텍스트 목록을 가져옵니다. 게시 컨텍스트는 컨텍스트에 대해 정의된 활성 서버가 하나 이상 있는 경우 활성 상태로 간주됩니다.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
TQID: 'https://experienceleague.adobe.com/g337PVX5asvB-o-VQL0XA5XSrgQ0c2vx0xC4-93Dm8E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 108
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
| contextArray | `types:StringArray` | 예 | 게시 컨텍스트에서 0개 이상의 값을 포함할 수 있는 활성 게시 컨텍스트의 배열입니다. |

