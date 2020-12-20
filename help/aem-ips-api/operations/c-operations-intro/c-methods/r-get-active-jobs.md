---
description: 현재 활성 작업을 모두 가져옵니다.
seo-description: 현재 활성 작업을 모두 가져옵니다.
seo-title: getActiveJobs
solution: Experience Manager
title: getActiveJobs
topic: Scene7 Image Production System API
uuid: 3231d349-b254-4dd0-804d-8beaab116b56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 15%

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
| ` *`companyHandle`*` | `xsd:string` | 아니요 | 회사의 손잡이입니다. |
| ` *`jobHandle`*` | `xsd:string` | 아니요 | 작업에 대한 핸들입니다. |
| ` *`originalName`*` | `xsd:string` | 아니요 | 원래 작업 이름. |

**출력(getActiveJobsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`jobArray`*` | `xsd:string` | 예 | 활성 작업 배열입니다. |

## 예제 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

이 코드 샘플은 IPS에서 실행 중인 회사의 모든 활성 작업을 반환합니다. 이 경우 IPS 예약 코디네이터가 실행 중인 활성 작업이 없는 상태로 비활성화되어 응답이 이례적인 경우입니다. 정상적인 상황에서 응답으로 많은 활성 작업이 반환됩니다.

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

