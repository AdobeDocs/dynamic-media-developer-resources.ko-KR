---
description: 실행하도록 예약된 작업을 가져옵니다.
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
TQID: 'https://experienceleague.adobe.com/DNUaAhcCeO8MvLH5YF5-WTA74fCyRKLxvXBKu0ltngk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 20%

---

# getScheduledJobs{#getscheduledjobs}

실행하도록 예약된 작업을 가져옵니다.

구문

## 승인된 사용자 유형 {#section-bd1835ab508a429f8143b3bdb811d6a4}

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
| company핸들 | `xsd:string` | 예 | 회사 손잡이. |
| jobHandle | `xsd:string` | 아니요 | 작업 핸들. |
| 원래 이름 | `xsd:string` | 아니요 | `submitJob`에 의해 지정된 이름입니다. |

**출력(getScheduledJobsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| jobArray | `types:ScheduledJobArray` | 예 | 예약된 작업의 배열입니다. |

## 예제 {#section-e79e7da86ba848fd9996aa36de462e6c}

이 코드 샘플은 작업 배열의 모든 예약된 작업을 반환합니다. 배열 자체에는 작업에 대한 자세한 정보가 포함되어 있습니다.

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
