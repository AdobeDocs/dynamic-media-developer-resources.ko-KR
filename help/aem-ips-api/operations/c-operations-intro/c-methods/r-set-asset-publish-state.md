---
description: 에셋을 게시할 준비가 되었는지 여부를 결정합니다.
solution: Experience Manager
title: setAssetPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 0dc195ee-9229-40a3-ad8b-8f00c2c9ff97
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 11%

---

# setAssetPublishState{#setassetpublishstate}

에셋을 게시할 준비가 되었는지 여부를 결정합니다.

구문

## 승인된 사용자 유형 {#section-11bec77e50b24461bb8c8aacf016eec8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 에셋에 대한 읽기 및 쓰기 권한이 있어야 합니다.

## 매개 변수 {#section-09d2ba001a2a455a9102550272f3eecb}

**입력(setAssetPublishStateParam)**

<table id="table_23CB72BFB8984CDF82D7207E7D82FC43"> 
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
   <td colname="col4"> 회사 손잡이. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 에셋 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4">사용 가능한 상태: 
    <ul id="ul_A2614608DF1E4DB6BF8141D33E59D180"> 
     <li id="li_8C90BFEEE2B14A0184F342018C45EE67"><span class="codeph"> MarkedForPublish</span> </li> 
     <li id="li_C4BC12B304DA4763956C3049AF597D06"><span class="codeph"> NotMarkedForPublish</span> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> contextHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

**출력**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-c31ead6d0e594317a12c120509527792}

이 코드 샘플은 `NotMarkedForPublish`을(를) 사용하여 에셋의 게시 상태를 설정합니다.

**요청**

```java
<setAssetPublishStateParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <publishState>NotMarkedForPublish</publishState>
</setAssetPublishStateParam>
```

**응답**

없음.
