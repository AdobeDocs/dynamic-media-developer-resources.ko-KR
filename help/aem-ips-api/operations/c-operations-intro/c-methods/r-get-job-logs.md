---
description: 선택한 회사에 대해 지정된 작업 로그를 가져옵니다. 문자, 방향, 시작 및 종료 날짜, 행 수별로 정렬할 수 있습니다.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 10%

---

# getJobLogs{#getjoblogs}

선택한 회사에 대해 지정된 작업 로그를 가져옵니다. 문자, 방향, 시작 및 종료 날짜, 행 수별로 정렬할 수 있습니다.

구문

## 승인된 사용자 유형 {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-8cfdc7994da24678a45edcb37e9a2166}

**입력(getJobLogsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 아니요 | 회사가 처리합니다. |
| 사용자 핸들 | `xsd:string` | 아니요 | 특정 사용자가 제출한 작업에 대한 로그를 가져옵니다. |
| 정렬 기준 | `xsd:string` | 아니요 | 정렬 필드를 선택할 수 있습니다. |
| sortDirection | `xsd:string` | 아니요 | 정렬 순서(오름차순 또는 내림차순). |
| startDate | `xsd:dateTime` | 아니요 | 작업 로그 시작 날짜 및 시간입니다. 이 필드에 대한 요청과 함께 시간대를 제공합니다. |
| endDate | `xsd:dateTime` | 아니요 | 작업 로그 종료 날짜 및 시간입니다. 이 필드에 대한 요청과 함께 시간대를 제공합니다. |
| numRows | `xsd:int` | 아니요 | 반환할 최대 행 수. |

**출력(getJobLogsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 작업 로그 배열 | `types: JobLogArray` | 예 | 작업 로그 배열. |

## 예제 {#section-35871c94b4a44559912577efddbc46a6}

이 코드 샘플은 특정 회사에 대한 IPS 작업 로그를 반환합니다. 특정 사용자 또는 회사 및 사용자에 대한 작업 로그를 반환하는 데도 사용할 수 있습니다.

**요청**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**응답**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```
