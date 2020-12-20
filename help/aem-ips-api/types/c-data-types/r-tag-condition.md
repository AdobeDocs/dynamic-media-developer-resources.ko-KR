---
description: 태그 필드에 대한 검색 조건을 정의합니다.
seo-description: 태그 필드에 대한 검색 조건을 정의합니다.
seo-title: TagCondition
solution: Experience Manager
title: TagCondition
topic: Scene7 Image Production System API
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 3%

---


# TagCondition{#tagcondition}

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
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 태그 필드 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">태그 필드 유형과 값 또는 valueArray 필드의 사용 여부에 따라 달라집니다. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5"><span class="codeph"> 값</span>이 전달되면 <span class="codeph"> op</span>은(는) 문자열 상수 Matches여야 합니다. 조건은 태그 값과 연결된 모든 자산과 일치합니다. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD"><span class="codeph"> valueArray</span>이 전달되면, 여는 필드는 단일 또는 여러 값이 있는 태그 필드에 대해 <span class="codeph"> MatchesAny</span> 상수가 될 수 있습니다. <span class="codeph"> MatchesAny</span> 조건은 <span class="codeph"> valueArray</span>에 있는 태그 값 중 적어도 하나에 연결된 모든 에셋과 일치합니다. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">다중값 태그 필드의 경우, 상위 필드를 <span class="codeph"> valueArray</span> 필드가 있는 상수 <span class="codeph"> MatchesAll</span>으로 설정할 수 있습니다. 이 경우 조건은 <span class="codeph"> valueArray</span>(다른 태그 값 외에 다른 태그 값 포함)의 모든 태그 값과 연결된 자산만 일치시킵니다. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 일치하는 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 일치하는 값이 여러 개 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

