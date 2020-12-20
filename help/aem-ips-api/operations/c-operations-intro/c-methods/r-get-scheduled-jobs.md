---
description: 실행되도록 예약된 작업을 가져옵니다.
seo-description: 실행되도록 예약된 작업을 가져옵니다.
seo-title: getScheduledJobs
solution: Experience Manager
title: getScheduledJobs
topic: Scene7 Image Production System API
uuid: 56b0623b-46d7-4d11-8eea-6543ed364b53
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 20%

---


# getScheduledJobs{#getscheduledjobs}

실행되도록 예약된 작업을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-2af604ff8282460990b9237158187f8f}

**입력(getScheduledJobsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사의 손잡이입니다. |
| ` *`jobHandle`*` | `xsd:string` | 아니요 | 작업 핸들. |
| ` *`originalName`*` | `xsd:string` | 아니요 | `submitJob`에서 지정한 이름입니다. |

**출력(getScheduledJobsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`jobArray`*` | `types:ScheduledJobArray` | 예 | 예약된 작업 배열입니다. |

## 예제 {#section-e79e7da86ba848fd9996aa36de462e6c}

이 코드 샘플은 작업 배열의 예약된 모든 작업을 반환합니다. 배열 자체에는 작업에 대한 자세한 정보가 포함되어 있습니다.

**요청**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**응답**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```

