---
description: 태그 필드에 대한 검색 조건을 정의합니다.
seo-description: 태그 필드에 대한 검색 조건을 정의합니다.
seo-title: 태그 조건
solution: Experience Manager
title: 태그 조건
topic: Scene7 Image Production System API
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 태그 조건{#tagcondition}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 태그 필드 핸들 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">태그 필드 유형 및 값 또는 valueArray 필드의 사용 여부에 따라 달라집니다. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">값이 <span class="codeph"> 전달되면</span> op <span class="codeph"></span> 는 문자열 상수 Matches여야 합니다. 조건은 태그 값과 연결된 모든 자산과 일치합니다. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">value <span class="codeph"> Array</span> 가 전달되면, 여는 필드가 단일 또는 다중 값 태그 필드에 대한 <span class="codeph"></span> 상수 MatchesAny가 될 수 있습니다. 일치모든 <span class="codeph"> 조건은 값 배열의 태그 값 중 하나 이상에 연결된 모든 자산과</span> 일치합니다 <span class="codeph"></span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">다중 값 태그 필드의 경우, op 필드를 value Array <span class="codeph"> 필드를 사용하여</span> 상수 MatchesAll로 설정할 <span class="codeph"> 수</span> 있습니다. 이 경우, 조건은 valueArray의 모든 태그 값과 연결된 자산만 <span class="codeph"> 일치시킵니다</span> (다른 태그 값 외에도 가능). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 값</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 일치하는 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> valueArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 일치하는 값이 여러 개 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

