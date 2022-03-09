---
description: 현재 활성 작업을 모두 가져옵니다.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 16%

---

# getActiveJobs{#getactivejobs}

현재 활성 작업을 모두 가져옵니다.

구문

## 인증된 사용자 유형 {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**입력(getActiveJobsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 아니요 | 회사의 손잡이입니다. |
| jobHandle | `xsd:string` | 아니요 | 작업 핸들입니다. |
| originalName | `xsd:string` | 아니요 | 원래 작업 이름입니다. |

**출력(getActiveJobsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| jobArray | `xsd:string` | 예 | 활성 작업의 배열입니다. |

## 예제 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

이 코드 샘플은 IPS를 실행하는 회사의 모든 활성 작업을 반환합니다. 이 경우 IPS 예약 코디네이터가 실행 중인 활성 작업이 없는 상태로 비활성화되어 응답이 이례적인 경우 일반적인 상황에서 응답은 많은 활성 작업을 반환합니다.

**요청**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**응답**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```
