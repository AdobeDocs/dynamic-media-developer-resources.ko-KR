---
title: removeFolderPermissions
description: 폴더 권한을 제거합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 10830980-d504-4610-96c9-730937453256
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---

# removeFolderPermissions{#removefolderpermissions}

폴더 권한을 제거합니다.

구문

## 승인된 사용자 유형 {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-7efa68377fd846219b906d354ae64ed3}

**입력(removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 필수 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 제거할 권한이 있는 폴더가 있는 회사의 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 폴더에 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> <p><span class="codeph">이(가) true</span>인 경우: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">권한 제거가 모든 폴더 권한 작업을 통해 전파됩니다. </li> 
     </ul> </p> <p><span class="codeph"> false</span>일 때: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">이 작업은 지정된 폴더에만 영향을 줍니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(removeFolderPermissionsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-04390f0ec7cc460cb5d34d518e33e7a5}

이 코드 샘플은 폴더 및 그 하위 폴더에서 권한을 제거합니다. 상위 폴더에서만 권한을 제거하려면 `updateChildren`을(를) `false`(으)로 설정하십시오.

**요청**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**응답**

없음.
