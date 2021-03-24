---
description: PropertySetType 및 createPropertySetTypeParam 필드에 유효한 값입니다.
solution: Experience Manager
title: PropertySetType
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 4%

---


# PropertySetType{#propertysettype}

PropertySetType 및 createPropertySetTypeParam 필드에 유효한 값입니다.

값은 다음과 같습니다.

* `UserProperty`
* `CompanyProperty`
* `UserCompanyProperty`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 문자 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">회사 핸들. <p>참고: 회사 핸들이 없는 경우 유형은 global입니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 이름을 입력합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">속성 집합 유형 중 하나입니다. 입력(<span class="codeph"> createPropertySetTypeParam</span>)을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> allowMultiple</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 여러 속성 집합 인스턴스를 이 유형의 개체에 첨부할 수 있도록 허용할지 여부. </td> 
  </tr> 
 </tbody> 
</table>

