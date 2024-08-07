---
description: 관련 에셋 그룹에 대한 프로젝트를 가져옵니다.
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7262ed7-7419-4d6b-86ed-f3ad4657d654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 19%

---

# getProjects{#getprojects}

관련 에셋 그룹에 대한 프로젝트를 가져옵니다.

구문

## 승인된 사용자 유형 {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-8d549237b8c440b4872a0a086ddc00a1}

**입력(getProjectsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 손잡이. |

**출력(getProjectsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| projectArray | `types:ProjectArray` | 예 | 회사와 연계된 프로젝트 배열. |

## 예제 {#section-8b12d0b948f644f68bf9a16060d3849a}

이 코드 샘플은 프로젝트 배열의 모든 프로젝트 핸들을 반환합니다.

**요청**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**응답**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```
