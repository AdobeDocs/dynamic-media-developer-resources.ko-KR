---
description: 하나 이상의 에셋에 대한 게시 상태를 재설정하여 에셋을 다음 게시 작업에 강제로 다시 게시합니다.
solution: Experience Manager
title: forceRepublishAssets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4c75af38-4791-4f21-8d1b-4855fcdfd4b1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 9%

---

# forceRepublishAssets{#forcerepublishassets}

하나 이상의 에셋에 대한 게시 상태를 재설정하여 에셋을 다음 게시 작업에 강제로 다시 게시합니다.

구문

## 승인된 사용자 유형 {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**입력(forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> company핸들</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>재설정할 자산이 포함된 회사에 대해 을(를) 처리합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:부울</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>에셋의 파일이 게재 서버에 다시 게시되도록 지정합니다. 기본값은 입니다. <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> 카탈로그 재동기화</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:부울</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>자산을 제공하는 데 사용되는 카탈로그 메타데이터가 동기화되어 최신 상태를 보장하도록 지정합니다. 이 매개 변수는 동일한 레코드에 대한 거의 동시 업데이트 시 발생할 수 있는 경합 조건을 해결하는 데 사용됩니다. 기본값은 입니다. <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>게시 상태를 재설정할 자산의 핸들 배열입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>게시 상태 업데이트 배열. </p> </td> 
  </tr> 
 </tbody> 
</table>
