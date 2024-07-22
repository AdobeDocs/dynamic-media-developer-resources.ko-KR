---
description: 일시 중지된 작업을 다시 시작합니다.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 14%

---

# resumeJob{#resumejob}

일시 중지된 작업을 다시 시작합니다.

구문

## 승인된 사용자 유형 {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**입력(resumeJobParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 다시 시작할 작업이 있는 회사에 대한 핸들입니다. |
| jobHandle | `xsd:string` | 예 | 일시 중지된 작업에 대한 핸들입니다. |

**출력(resumeJobReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-d0524e031f1f43d89430eade19526162}

이 코드 샘플은 일시 중지된 작업을 다시 시작합니다.

**요청**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**응답**

없음.
