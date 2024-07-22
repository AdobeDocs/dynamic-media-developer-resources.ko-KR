---
description: 회사 핸들, 회사 이름, 루트 경로 및 만료 날짜를 포함하여 지정된 회사에 대한 정보를 반환합니다. 정보를 검색할 companyHandle 또는 companyName을 지정해야 합니다.
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72bd223b-c99a-48a3-9c0a-d1af392d904c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 7%

---

# getCompanyInfo{#getcompanyinfo}

회사 핸들, 회사 이름, 루트 경로 및 만료 날짜를 포함하여 지정된 회사에 대한 정보를 반환합니다. 정보를 검색할 companyHandle 또는 companyName을 지정해야 합니다.

구문

## 승인된 사용자 유형 {#section-74f20fb8602e4f96810795bc4b6f7fdf}

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> 또는 <span class="codeph"> <span class="varname"> companyName</span> </span>이(가) 필요합니다. </p> </td> 
   <td colname="col4"> <p>정보를 얻고자 하는 회사의 핸들입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> 또는 <span class="codeph"> <span class="varname"> companyName</span> </span>이(가) 필요합니다. </p> </td> 
   <td colname="col4"> <p>정보를 얻으려는 회사의 이름입니다. </p> </td> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
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
