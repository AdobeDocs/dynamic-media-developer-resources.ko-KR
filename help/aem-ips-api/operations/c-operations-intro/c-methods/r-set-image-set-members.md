---
description: 이미지 세트와 관련된 자산 목록을 설정합니다.
seo-description: 이미지 세트와 관련된 자산 목록을 설정합니다.
seo-title: setImageSetMembers
solution: Experience Manager
title: setImageSetMembers
topic: Scene7 Image Production System API
uuid: 84a73ff4-e93f-4764-80e8-e15f1fec1aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setImageSetMembers{#setimagesetmembers}

이미지 세트와 관련된 자산 목록을 설정합니다.

이 작업은 에 대한 `pageReset` 매개 변수를 `ImageSets` 무시하고 `SpinSets` 값을 true로 강제 적용합니다.

## 인증된 사용자 유형 {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 이미지 집합 자산에 대한 읽기 및 쓰기 액세스 권한과 각 구성원 자산에 대한 읽기 액세스 권한이 있어야 합니다.

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
   <td colname="col1"> <p><span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>회사 핸들 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자산 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 세트 핸들 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> memberArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 세트에 속하는 자산 멤버의 배열입니다. </td> 
  </tr> 
 </tbody> 
</table>

**출력(setImageSetMembersReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-7b87219034464aa98524178ccee27738}

이 코드 샘플은 멤버 배열을 사용하여 이미지 세트의 멤버를 설정합니다.

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
