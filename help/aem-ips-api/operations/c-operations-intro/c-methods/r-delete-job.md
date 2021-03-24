---
description: 현재 또는 예약된 작업을 삭제합니다.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 12%

---


# deleteJob{#deletejob}

현재 또는 예약된 작업을 삭제합니다.

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
| `*`companyHandle`*` | `xsd:string` | 예 | 작업이 속한 회사의 핸들. |
| `*`jobHandle`*` | `xsd:string` | 예 | 삭제할 작업에 대한 핸들입니다. |

**출력**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

이 코드 샘플은 실행 중이거나 IPS에서 실행되도록 예약된 작업을 삭제합니다. 다른 작업에서 얻어야 하는 작업 핸들이 필요합니다.

**요청**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**응답**

없음.
