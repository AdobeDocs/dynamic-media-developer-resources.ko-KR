---
description: 이미지 세트와 연결된 에셋 목록을 설정합니다.
solution: Experience Manager
title: setImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: c30df5fe-e355-45d4-8c06-e396caca0d58
TQID: 'https://experienceleague.adobe.com/nacym3xe-m5gu-Hi2Gqkz-O03-CbqB9B-uCDRVkhrvc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 8%

---

# setImageSetMember{#setimagesetmembers}

이미지 세트와 연결된 에셋 목록을 설정합니다.

이 작업은 `ImageSets` 및 `SpinSets`에 대한 `pageReset` 매개 변수를 무시하고 값을 true로 강제 적용합니다.

## 승인된 사용자 유형 {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 이미지 집합 에셋에 대한 읽기 및 쓰기 액세스 권한과 각 멤버 에셋에 대한 읽기 액세스 권한을 보유해야 합니다.

## 매개 변수 {#section-2f46efcd24c648aeacba738509426e46}

**입력(setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>회사 핸들. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 집합 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 형식:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 집합에 속하는 자산 멤버의 배열입니다. </td> 
  </tr> 
 </tbody> 
</table>

**출력(setImageSetMembersReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-7b87219034464aa98524178ccee27738}

이 코드 샘플은 멤버 배열을 사용하여 이미지 집합의 멤버를 설정합니다.

**요청**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**응답**

없음.
