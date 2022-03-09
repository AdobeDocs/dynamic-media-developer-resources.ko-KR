---
description: 현재 작업이나 예약된 작업을 삭제합니다.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---

# deleteJob{#deletejob}

현재 작업이나 예약된 작업을 삭제합니다.

구문

## 인증된 사용자 유형 {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-000c42bc93744b1a8e777f3ec3c272b0}

**입력(deleteJobParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 작업이 속한 회사의 핸들. |
| jobHandle | `xsd:string` | 예 | 삭제할 작업에 대한 핸들입니다. |

**출력**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

이 코드 샘플은 실행 중이거나 IPS에서 실행되도록 예약된 작업을 삭제합니다. 다른 작업에서 가져와야 하는 작업 핸들이 필요합니다.

**요청**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**응답**

없음.
