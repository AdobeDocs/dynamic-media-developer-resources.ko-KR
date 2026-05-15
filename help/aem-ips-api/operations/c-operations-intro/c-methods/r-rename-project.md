---
description: 프로젝트 이름을 변경합니다.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
TQID: 'https://experienceleague.adobe.com/FjPL1Xn4QAYYCdyeYKA1MiQVay988g-sbuiHpazhcMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 21%

---

# renameProject{#renameproject}

프로젝트 이름을 변경합니다.

구문

## 승인된 사용자 유형 {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-43ccd77648784be4a259a723c3e1db40}

**입력(renameProjectParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyName | `xsd:string` | 예 | 이름을 바꿀 프로젝트와 함께 회사를 처리합니다. |
| projectHandle | `xsd:string` | 예 | 프로젝트를 처리합니다. |
| projectName | `xsd:string` | 예 | 새 프로젝트 이름. |

**출력(renameProjectParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| projectHandle | `xsd:string` | 예 | 이름이 변경된 프로젝트의 핸들입니다. |

## 예제 {#section-a0a06d9244774795b695a10b92b2a5e7}

이 코드 샘플은 프로젝트 이름을 바꾸고 프로젝트 핸들을 반환합니다.

**요청**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**응답**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```
