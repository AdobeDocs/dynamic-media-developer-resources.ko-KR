---
description: 태그 필드에 대한 검색 조건을 정의합니다.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
TQID: 'https://experienceleague.adobe.com/5y2KRE0lZvEuY4wZmcJ-ZrKM5bM9OVwMeSdux9iQl6E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 156
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
   <td colname="col3"> 태그 필드 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 작업</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">태그 필드 유형과 value 또는 valueArray 필드의 사용 여부에 따라 다릅니다. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5"><span class="codeph"> 값</span>이(가) 전달되면 <span class="codeph"> op</span>은(는) 문자열 상수 Matches여야 합니다. 조건은 태그 값과 연결된 모든 자산과 일치합니다. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD"><span class="codeph"> valueArray</span>이(가) 전달되면 작업 필드는 단일 또는 다중 값 태그 필드에 대한 상수 <span class="codeph"> MatchesAny</span>일 수 있습니다. <span class="codeph"> MatchesAny</span> 조건이 <span class="codeph"> valueArray</span>의 태그 값 중 하나 이상과 연결된 모든 에셋과 일치합니다. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">다중 값 태그 필드의 경우 작업 필드를 <span class="codeph"> valueArray</span> 필드와 함께 상수 <span class="codeph"> MatchesAll</span>(으)로 설정할 수 있습니다. 이 경우 조건은 <span class="codeph"> valueArray</span>의 모든 태그 값과 연결된 에셋만 일치합니다(다른 태그 값과 함께). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 값</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 일치하는 값. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 형식:StringArray</span> </td> 
   <td colname="col3"> 일치하는 값이 여러 개 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

