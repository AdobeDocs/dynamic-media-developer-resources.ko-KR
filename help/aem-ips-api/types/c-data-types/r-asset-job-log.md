---
description: 특정 자산과 연관된 작업 로그 항목의 세부 정보입니다. getAssetJobLogs가 반환한 데이터입니다.
seo-description: 특정 자산과 연관된 작업 로그 항목의 세부 정보입니다. getAssetJobLogs가 반환한 데이터입니다.
seo-title: AssetJobLog
solution: Experience Manager
title: AssetJobLog
topic: Scene7 Image Production System API
uuid: 0dd65da1-f358-4d9a-98a2-abfb036347e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetJobLog{#assetjoblog}

특정 자산과 연관된 작업 로그 항목의 세부 정보입니다. getAssetJobLogs가 반환한 데이터입니다.

구문

## 매개 변수 {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 작업 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 작업 핸들 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 작업 <span class="varname"> 이름</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 작업 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 로그 <span class="varname"> 메시지</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">작업 로그의 메시지입니다. <p><span class="codeph"> logMessage</span> 응답 필드는 <span class="codeph"> authHeader 로케일 필드를 기반으로</span> 현지화됩니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 로그 <span class="varname"> 유형</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 로그 항목의 작업 유형입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> submitUserEmail <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 작업을 제출한 사용자의 전자 메일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 로그 <span class="varname"> 날짜</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 작업 날짜. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 보조</span> 배열 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:JobLogDetailArray</span> </td> 
   <td colname="col3"> 각 작업 로그에 대한 보조 작업 로그 메시지 배열입니다. </td> 
  </tr> 
 </tbody> 
</table>

