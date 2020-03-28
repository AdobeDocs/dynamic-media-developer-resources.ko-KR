---
description: 회사 작업 로그의 세부 정보를 가져옵니다.
seo-description: 회사 작업 로그의 세부 정보를 가져옵니다.
seo-title: getJobLogDetails
solution: Experience Manager
title: getJobLogDetails
topic: Scene7 Image Production System API
uuid: e4314348-2160-4775-a02f-b4892924f064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getJobLogDetails{#getjoblogdetails}

회사 작업 로그의 세부 정보를 가져옵니다.

응답 `logMessage` 필드는 `authHeader` `locale` 필드를 기준으로 현지화됩니다.

## 인증된 사용자 유형 {#section-6f720a7baad64eb3805868c88af9a960}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-47d411a755224c23a4521f10341d66ab}

**입력(getJobLogDetailsParam)**

<table id="table_A77122D73F684B3F8F5AFA1C11C189ED"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 필수 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 작업 로그가 속한 회사의 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 작업 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 활성 또는 완료된 작업의 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 원본</span> 이름 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 작업 로그의 원래 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> logTypeArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 하나 이상의 로그 유형 상수입니다. 있는 경우 지정된 로그 유형만 반환됩니다. 기본적으로 모든 로그 유형이 반환됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 페이지당 <span class="varname"> 레코드</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4">반환할 최대 <span class="codeph"> 세부 정보</span> 배열 항목 수입니다. 최대값과 기본값은 1000입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 결과</span> 페이지 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4">반환할 <span class="codeph"> PerPage</span>결과 페이지 수입니다. 기본값은 1입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 정렬 <span class="varname"> 기준</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>작업 세부 사항 정렬 필드 상수 값(날짜 또는 로그 유형) 중 하나. 기본값은 날짜입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 정렬 <span class="varname"> 방향</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>정렬 방향 문자열 상수 중 하나입니다. 기본값은 오름차순입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(getJobLogDetailsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`jobLogArray`*` | `types:JobLogArray` | 예 | 작업 로그 배열. |

## 예제 {#section-007678b8b8d94e8f91d09f6bc855f394}

이 코드 샘플은 특정 회사에 대한 모든 작업 로그 세부 정보를 반환합니다. 첫 번째 배열에는 표준 작업 로그 세부 사항이 포함됩니다. 포함된 배열은 작업에 대한 추가 정보를 반환합니다.

**요청**

```java
<ns1:getJobLogDetailsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:jobHandle>47||Add_2007-09-14-15:04:34</ns1:jobHandle>
</ns1:getJobLogDetailsParam>
```

**응답**

```java
<getJobLogDetailsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>some_address@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
         <detailArray>
            <items>
               <logMessage>Upload has begun!</logMessage>
               <logType>BeginUpload</logType>
            </items>
            <items>
               <logMessage>Add_2007-09-14-15:04:34</logMessage>
               <logType>OriginalJobName</logType>
            </items>
            <items>
               <logMessage>s7oslo</logMessage>
               <logType>JobClient</logType>
            </items>
            ...
         </detailArray>
      </items>
   </jobLogArray>
</getJobLogDetailsReturn>
```

