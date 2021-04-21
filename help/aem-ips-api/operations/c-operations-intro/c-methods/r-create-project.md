---
description: 새 프로젝트를 만듭니다.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 18%

---


# createProject{#createproject}

새 프로젝트를 만듭니다.

구문

## 인증된 사용자 유형 {#section-17878e2e4c3a44988c9a1af82c2ac319}

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
| `*`companyHandle`*` | `xsd:string` | 예 | 새 프로젝트와 연결된 회사의 취급입니다. |
| `*`projectName`*` | `xsd:string` | 예 | 새 프로젝트 이름. |

**출력(createProjectParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | 예 | 새 프로젝트의 핸들입니다. |

## 예제 {#section-a0cd532b67e346d088fbec141231a0e5}

이 코드 샘플은 해당 핸들에 의해 지정된 회사에 `ApiTestProject`이라는 프로젝트를 만듭니다. 응답은 프로젝트에 대한 핸들을 반환합니다.

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

