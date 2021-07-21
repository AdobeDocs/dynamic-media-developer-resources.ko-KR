---
description: 작업 진행 정보.
solution: Experience Manager
title: 작업 진행
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 35e3be1e-ccc2-460c-98c1-bbefab1df699
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---

# 작업 진행{#taskprogress}

작업 진행 정보.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 작업 유형 설명입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessed</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 이미 처리된 작업 항목 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 현재 진행 중인 작업 항목 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 보류 중인 작업 항목 수(아직 처리되지 않음). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 진행 중</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> % 진행률(범위 0.0 - 1.0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 진행 메시지. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 마지막 진행 정보가 마지막으로 업데이트된 시간입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:TaskItemProgressArray</span> </td> 
   <td colname="col3"> 작업 항목의 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">값은 다음과 같습니다. 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> 알 수 없음</span>: 작업 모니터가 상태 간에 전환될 때. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> 새로 만들기</span>: 작업 모니터가 만들어졌지만 아직 작업을 수락하지 않았습니다. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> 처리</span>: 작업 모니터가 작업을 처리하고 있습니다. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> 중지</span>: 작업 중지 요청으로 인해 작업 모니터가 작업을 중지하고 있습니다. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> 완료</span>: 작업 모니터 작업에 할당된 작업이 완료되었습니다. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> 실패</span>: 치명적인 오류를 나타냅니다. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
