---
description: PropertySetType 및 createPropertySetTypeParam 필드에 유효한 값입니다.
seo-description: PropertySetType 및 createPropertySetTypeParam 필드에 유효한 값입니다.
seo-title: PropertySetType
solution: Experience Manager
title: PropertySetType
topic: Scene7 Image Production System API
uuid: 83220180-3272-4552-974d-a73e6aad3483
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 문자 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">회사 핸들 <p>참고: 회사 핸들이 없는 경우 유형이 글로벌입니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 유형 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 속성 <span class="varname"> 유형</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">속성 집합 유형 중 하나입니다. 입력(createPropertySetTypeParam<span class="codeph"> )을</span>참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 다중 <span class="varname"> 허용</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 여러 속성 집합 인스턴스를 이 유형의 개체에 연결할지 여부. </td> 
  </tr> 
 </tbody> 
</table>

