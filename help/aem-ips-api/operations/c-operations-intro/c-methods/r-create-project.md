---
description: 새 프로젝트를 만듭니다.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 19%

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

이 코드 샘플은 `ApiTestProject` 을(를) 핸들로 지정한 회사에 포함합니다. 응답이 프로젝트에 대한 핸들을 반환합니다.

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
