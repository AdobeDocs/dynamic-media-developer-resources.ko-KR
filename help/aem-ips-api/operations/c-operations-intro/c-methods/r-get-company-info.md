---
description: 회사 핸들, 회사 이름, 루트 경로 및 만료 날짜를 포함하여 지정된 회사에 대한 정보를 반환합니다. 검색할 정보의 companyHandle 또는 companyName을 지정해야 합니다.
seo-description: 회사 핸들, 회사 이름, 루트 경로 및 만료 날짜를 포함하여 지정된 회사에 대한 정보를 반환합니다. 검색할 정보의 companyHandle 또는 companyName을 지정해야 합니다.
seo-title: getCompanyInfo
solution: Experience Manager
title: getCompanyInfo
topic: Scene7 Image Production System API
uuid: 9218cba8-2873-46b7-90e3-7ab9d5018690
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getCompanyInfo{#getcompanyinfo}

회사 핸들, 회사 이름, 루트 경로 및 만료 날짜를 포함하여 지정된 회사에 대한 정보를 반환합니다. 검색할 정보의 companyHandle 또는 companyName을 지정해야 합니다.

구문

## 인증된 사용자 유형 {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-7dec8871c89a414c9f066adade1831d8}

**입력(getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>필수 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>company <span class="codeph"> Handle <span class="varname"></span> 또는 </span> companyName <span class="codeph"> 이 <span class="varname"> 필요합니다</span> </span> . </p> </td> 
   <td colname="col4"> <p>정보를 얻고자 하는 회사의 취급자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 회사 <span class="varname"> 이름</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>company <span class="codeph"> Handle <span class="varname"></span> 또는 </span> companyName <span class="codeph"> 이 <span class="varname"> 필요합니다</span> </span> . </p> </td> 
   <td colname="col4"> <p>정보를 받으려는 회사의 이름입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>필수 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 회사 <span class="varname"> 정보</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:회사</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>회사에 대한 기타 설명 정보를 처리합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예제 {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

이 코드 샘플은 회사 이름과 핸들을 사용하여 회사에 대한 모든 정보를 반환합니다. 회사를 만들 때 받은 응답과 유사한 데이터를 반환합니다.

**요청**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**응답**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```

