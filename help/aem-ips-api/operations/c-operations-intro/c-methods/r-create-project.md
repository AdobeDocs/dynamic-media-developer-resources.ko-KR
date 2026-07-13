---
description: 새 프로젝트를 만듭니다.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
TQID: 'https://experienceleague.adobe.com/GKNImvhmX1bOepsV0-6QzgZr5jskJQlaqXCMIT5ue5M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 18%

---

# createProject{#createproject}

새 프로젝트를 만듭니다.

구문

## 승인된 사용자 유형 {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-8c741884eb54489bbaad0c444fee80b6}

**입력(createProjectParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 새 프로젝트와 연계된 회사의 핸들입니다. |
| projectName | `xsd:string` | 예 | 새 프로젝트 이름. |

**출력(createProjectParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| projectHandle | `xsd:string` | 예 | 새 프로젝트에 대한 핸들입니다. |

## 예제 {#section-a0cd532b67e346d088fbec141231a0e5}

이 코드 샘플은 핸들로 지정된 회사에 `ApiTestProject`(이)라는 프로젝트를 만듭니다. 응답이 프로젝트에 대한 핸들을 반환합니다.

**요청**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```

