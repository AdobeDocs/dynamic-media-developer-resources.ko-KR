---
description: 여러 자산을 서로 독립적으로 이동합니다. 이 작업은 assetMoveArray에 포함된 AssetMove 형식을 사용하여 수행됩니다. 각 AssetMove 필드에는 대상 폴더가 포함되어 있습니다.
seo-description: 여러 자산을 서로 독립적으로 이동합니다. 이 작업은 assetMoveArray에 포함된 AssetMove 형식을 사용하여 수행됩니다. 각 AssetMove 필드에는 대상 폴더가 포함되어 있습니다.
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Scene7 Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 8%

---


# moveAssets{#moveassets}

여러 자산을 서로 독립적으로 이동합니다. 이 작업은 assetMoveArray에 포함된 AssetMove 형식을 사용하여 수행됩니다. 각 AssetMove 필드에는 대상 폴더가 포함되어 있습니다.

구문

## 인증된 사용자 유형 {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-7d47f663474b41cc83439288ac133cc5}

**입력(moveAssetsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 이동할 자산이 있는 회사에 대한 핸들입니다. |
| ` *`assetMoveArray`*` | `types:AssetMoveArray` | 예 | 자산 이동 배열입니다. 자산 및 자산 대상 폴더가 포함되어 있습니다. |

**출력(moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 자산 수를 이동했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 작업을 이동하려고 할 때 경고를 생성한 자산의 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 작업을 이동하려고 할 때 오류를 생성한 자산의 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <span class="codeph"> 다음</span>을 포함하는 AssetOperationFaults: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">경고를 던진 에셋입니다. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">경고 코드. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">경고에 대한 설명입니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <span class="codeph"> 다음</span>을 포함하는 AssetOperationFaults: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">오류를 발생시킨 자산입니다. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">오류 코드. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">오류 이유. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 예제 {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

이 코드 샘플은 자산을 `assetMoveArray`에서 지정한 특정 위치로 이동합니다. 배열에 자산 핸들 및 폴더 핸들이 포함되어 있습니다. 응답은 자산이 성공적으로 이동되었음을 나타냅니다.

**요청**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**응답**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

