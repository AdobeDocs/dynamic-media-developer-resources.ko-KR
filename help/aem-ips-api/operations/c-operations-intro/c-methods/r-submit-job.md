---
description: 시스템에 작업을 제출합니다.
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 7%

---

# submitJob{#submitjob}

시스템에 작업을 제출합니다.

구문

## 승인된 사용자 유형 {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-31a07dbccf964850883e817384499459}

**입력(submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>필수 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> <p>회사 핸들. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>작업을 제출한 사용자에게 처리합니다. </p> <p> <p>참고: 시스템에서 <span class="codeph"> userHandle</span>이(가) 지정한 사용자에게 전자 메일을 보냅니다. <span class="codeph"> userHandle</span>이(가) 제공되지 않으면 작업을 제출한 사람이 전자 메일을 받습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> <p>작업 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 로케일</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>작업 로그 세부 정보 및 이메일 현지화에 사용되는 로케일. </p> <p>로케일은 <span class="codeph"> &lt;language_code&gt;</span> 및 <span class="codeph"> [&lt;country_code&gt;]</span>(으)로 지정되었습니다. 여기서 언어 코드는 ISO-639에 지정된 소문자로 된 두 자리 코드이며 선택적 국가 코드는 ISO-3166에 지정된 소문자로 된 두 자리 코드입니다.) 예를 들어 영어(미국)에 대한 로케일 문자열은 en-US입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>작업 실행 날짜 및 시간입니다. </p> <p>참고: 요청의 시간대를 제공합니다. 시간대는 대상 IPS 서버의 시간대로 조정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>작업을 실행할 시기를 결정합니다. </p> <p> 반복해서 작업을 실행하는 <span class="codeph"> cron</span> 문자열일 수 있습니다. </p> <p>일정은 항상 서버의 현지 시간대를 기준으로 합니다. 사용자 지정 일정 형식에 대해서는 IPS 설명서를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 설명</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>작업 설명. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ExportJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>이전에 업로드한 파일을 내보냅니다. </p> <p><a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageServingPublishJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>이미지 제공 게시 작업에 대한 세부 정보. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>이미지 렌더링 게시 작업에 대한 세부 정보. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:VideoPublishJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>비디오 게시 작업에 대한 세부 정보. </p> <p><a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>서버 디렉토리 게시 작업에 대한 세부 정보. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UploadDirectoryJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>업로드 디렉터리 작업에 대한 세부 정보. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UploadUrlsJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>업로드 URL 작업에 대한 세부 정보. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:OptimizeImagesJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:RipPdfsJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>자동화된 집합 스크립트를 사용하여 자산 목록을 집합으로 처리합니다. </p> <p><a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(submitJobReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| jobHandle | `xsd:string` | 예 | 작업 핸들. |

## 예제 {#section-40ac77d14adf4588ba2575be6879b2d2}

이 코드 샘플은 게시 작업을 제공하는 이미지를 IPS에 제출하고 작업 핸들을 반환합니다. 요청에서 작업 유형을 하나만 선택하십시오. `userHandle`이(가) 생략되었으므로 작업을 제출한 사용자에게 전자 메일 알림이 전송됩니다. `execTime` 및 `execSchedule`이(가) 생략되었으므로 이 샘플 작업이 즉시 실행됩니다.

**요청**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**응답**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## 주의 {#section-0f3078e503a249aeb6f3d662a51f036a}

`execTime` 및 `execSchedule` 중 하나만 지정할 수 있습니다. 둘 다 전달되지 않으면 작업이 즉시 실행됩니다. 다음 중 하나만 사용할 수 있습니다.

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
