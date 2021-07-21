---
description: setAssetMetadata에 사용되는 특정 자산에 대한 메타데이터 값을 설정합니다. 메타데이터에 적용할 변경 사항을 설명합니다.
solution: Experience Manager
title: MetadataUpdate
feature: Dynamic Media Classic,SDK/API,메타데이터
role: Developer,Admin
exl-id: 99dc1f0c-c4c4-433e-9b91-fa39ef6f84d7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 1%

---

# MetadataUpdate{#metadataupdate}

setAssetMetadata에 사용되는 특정 자산에 대한 메타데이터 값을 설정합니다. 메타데이터에 적용할 변경 사항을 설명합니다.

>[!NOTE]
>
>단일 값 필드가 전달되면 자산의 태그 값이 지정된 태그 값으로 재설정됩니다.

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
   <td colname="col3"> 메타데이터 필드 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 메타데이터 업데이트 값. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:부울</span> </td> 
   <td colname="col3"> 부울 메타데이터 값(부울 형식 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 긴 메타데이터 값(int 형식 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> 이중 메타데이터 값(부동 소수점 형식 필드만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 날짜 메타데이터 값(날짜 형식 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:StringArray</span> </td> 
   <td colname="col3"> <p>자산의 기존 태그 값 목록에 을 추가합니다. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">단일 값 태그 필드는 마지막 값만 저장합니다. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">값이 사전에 없으면 고정된 사전 태그 필드에 오류가 반환됩니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:StringArray</span> </td> 
   <td colname="col3">자산에 대한 기존 태그 값 목록을 대체합니다. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">단일 값 태그 필드는 마지막 값만 저장합니다. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">값이 사전에 없으면 고정된 사전 태그 필드에 오류가 반환됩니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:StringArray</span> </td> 
   <td colname="col3"> 자산의 태그 값 목록에서 지정된 값이 있는 경우 삭제합니다. </td> 
  </tr> 
 </tbody> 
</table>
