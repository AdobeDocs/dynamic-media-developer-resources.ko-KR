---
description: 그룹 배열에 사용자를 추가합니다.
seo-description: 그룹 배열에 사용자를 추가합니다.
seo-title: addGroupMembership
solution: Experience Manager
title: addGroupMembership
topic: Scene7 Image Production System API
uuid: a8e25f27-c300-424d-83ac-e41bb4cb7964
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addGroupMembership{#addgroupmembership}

그룹 배열에 사용자를 추가합니다.

구문

## 인증된 사용자 유형 {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-e250f6ddb13646808c6a8860b6442bc5}

**입력(addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> 사용자 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>그룹 구성원을 추가할 사용자를 처리합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> groupHandleArray <span class="varname"> 그룹</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>회사가 속할 그룹에 대한 핸들 배열입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(add 파섹**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-f7a1f40c3d7a40ea964b29056c734d81}

이 예제에서는 groupHandleArray가 있는 회사에 그룹을 ` *`추가합니다`*`. 이 예에서는 하나의 그룹만 사용합니다.

**요청**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**응답**

없음.
