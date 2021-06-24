---
description: 시스템에 회사를 추가합니다.
solution: Experience Manager
title: addCompany
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 2f834fe8-a621-4a41-9473-8ef53294b348
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 9%

---

# addCompany{#addcompany}

시스템에 회사를 추가합니다.

시스템에 추가할 회사의 이름을 보내고 선택적으로 회사가 만료되는지 여부를 보냅니다.

이 작업이 호출되면 시스템은 회사 핸들과 설명 필드를 포함하는 `*`companyInfo`*` 유형을 가져옵니다. 요청한 회사 이름이 시스템에 이미 있으면 `ipsApiFault`이 발생합니다.

## 인증된 사용자 유형 {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-c64a21b72585447880760db9e7a12ccb}

**입력(addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>추가할 회사의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> expires</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>회사의 만료 날짜입니다. 이 필드에 대한 요청을 시간대를 제공합니다. 시간대는 중부 시간으로 조정됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
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
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>새 회사의 및 이름, 루트 경로, 만료 날짜 및 시간을 처리합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예제 {#section-4c8f1bb40d154c77a7b410468206e52b}

이 예에서는 IPS 시스템에 회사를 추가하라는 요청과 다른 작업을 수행하는 데 필요한 추가된 회사에 대한 정보를 자세히 설명하는 응답을 보여줍니다.

**요청**

```java
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**응답**

```java
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```
