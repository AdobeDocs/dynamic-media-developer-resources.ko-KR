---
description: 자산을 게시할 준비가 되었는지 확인합니다.
seo-description: 자산을 게시할 준비가 되었는지 확인합니다.
seo-title: setAssetPublishState
solution: Experience Manager
title: setAssetPublishState
topic: Scene7 Image Production System API
uuid: b7d49d77-573c-4e2a-81d3-196c09d62853
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetPublishState{#setassetpublishstate}

자산을 게시할 준비가 되었는지 확인합니다.

구문

## 인증된 사용자 유형 {#section-11bec77e50b24461bb8c8aacf016eec8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-09d2ba001a2a455a9102550272f3eecb}

**입력(set 파섹**

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
   <td colname="col1"> <span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 회사의 손잡이입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자산 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 자산 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4">사용 가능한 상태: 
    <ul id="ul_A2614608DF1E4DB6BF8141D33E59D180"> 
     <li id="li_8C90BFEEE2B14A0184F342018C45EE67"><span class="codeph"> MarkedForPublish</span> </li> 
     <li id="li_C4BC12B304DA4763956C3049AF597D06"><span class="codeph"> NotMarkedForPublish</span> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> contextHandleArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

**출력**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-c31ead6d0e594317a12c120509527792}

이 코드 샘플은 를 사용하여 자산의 게시 상태를 설정합니다 `NotMarkedForPublish`.

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
