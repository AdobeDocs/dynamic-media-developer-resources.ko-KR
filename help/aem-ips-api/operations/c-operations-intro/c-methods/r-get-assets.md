---
title: getAssets
description: IPS(이미지 프로덕션 시스템)에서 자산을 반환합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 3b63da9c-f10a-40bf-8e3c-4f0bfc53d74c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 12%

---

# getAssets{#getassets}

IPS(이미지 프로덕션 시스템)에서 자산을 반환합니다.

구문

## 승인된 사용자 유형 {#section-4673c1c9f4314160af8b165eb2dd20cc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자가 액세스할 수 있는 자산만 반환합니다.

## 매개 변수 {#section-bb9cf1ab19ea47acbd9ae58646dbe273}

**입력(getAssetsParam)**

<table id="table_15CDEFC7F836411C80AA122E3A701C77"> 
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
   <td colname="col4"> <p>회사가 처리합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>특정 사용자 가장. 관리자만 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>그룹별로 필터링합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>폴더 및 모든 하위 폴더를 리프 수준으로 검색할 루트 폴더입니다. 제외되는 경우 회사 루트가 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 형식:StringArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>응답에 포함된 필드 및 하위 필드. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 형식:StringArray</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>응답에서 제외된 필드 및 하위 필드. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(getAssetsReturn)**

<table id="table_694932BBBD2C4167871380B2CF514BEA"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:AssetArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>필터 조건과 일치하는 에셋 배열. </p> </td> 
  </tr> 
 </tbody> 
</table>
