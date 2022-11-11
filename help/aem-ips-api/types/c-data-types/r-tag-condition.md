---
description: 태그 필드에 대한 검색 조건을 정의합니다.
solution: Experience Manager
title: 태그 조건
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# [!DNL TagCondition]{#tagcondition}

태그 필드에 대한 검색 조건을 정의합니다.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 태그 필드 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">태그 필드 유형과 값 또는 valueArray 필드를 사용할지 여부에 따라 다릅니다. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">If <span class="codeph"> value</span> 가 전달되고, <span class="codeph"> op</span> 는 문자열 상수 Matches여야 합니다. 조건은 태그 값과 연결된 모든 자산과 일치합니다. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">If <span class="codeph"> valueArray</span> 가 전달되면 op 필드가 상수일 수 있습니다. <span class="codeph"> MatchesAny</span> 단일 또는 여러 값을 갖는 태그 필드에 대해 설명합니다. A <span class="codeph"> MatchesAny</span> 조건은 의 태그 값 중 하나 이상과 연결된 모든 자산과 일치합니다 <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">여러 값을 갖는 태그 필드의 경우 op 필드를 상수로 설정할 수 있습니다 <span class="codeph"> MatchesAll</span> 사용 <span class="codeph"> valueArray</span> 필드. 이 경우, 조건은 의 모든 태그 값과 연결된 자산만 일치시킵니다 <span class="codeph"> valueArray</span> (다른 태그 값 외에 있을 수 있음). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 일치하는 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:StringArray</span> </td> 
   <td colname="col3"> 일치하는 값이 여러 개 있습니다. </td> 
  </tr> 
 </tbody> 
</table>
