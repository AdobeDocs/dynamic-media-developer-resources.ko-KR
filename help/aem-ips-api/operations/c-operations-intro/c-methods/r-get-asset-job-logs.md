---
description: 자산에 대한 작업 로그를 가져옵니다. 배열에서 반환되는 항목에는 해당 에셋의 작업 로그에 있는 각 항목에 대한 자세한 정보가 들어 있습니다. logMessage 응답 필드는 authHeader 필드를 기반으로 현지화됩니다.
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 8%

---

# getAssetJobLogs{#getassetjoblogs}

자산에 대한 작업 로그를 가져옵니다. 배열에서 반환되는 항목에는 해당 에셋의 작업 로그에 있는 각 항목에 대한 자세한 정보가 들어 있습니다. logMessage 응답 필드는 authHeader 필드를 기반으로 현지화됩니다.

구문

## 승인된 사용자 유형 {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-9586617e124b4da4acb6b66b2a9adad8}

**입력(getAssetJobLogsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 자산이 속한 회사에 대한 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 검색할 작업 로그가 있는 에셋에 대한 핸들입니다. |

**출력(getAssetJobLogsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 작업 로그 배열 | `types:AssetJobLogArray` | 예 | 작업 로그 배열입니다. |

## 예제 {#section-f03d7f3ec5d043d38227f926fb7609f6}

이 코드 샘플은 특정 자산의 작업 로그를 검색합니다. 응답은 자산이 사용된 모든 작업에 대한 자세한 정보가 포함된 작업 로그 배열을 반환합니다.

**요청**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**응답**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```
