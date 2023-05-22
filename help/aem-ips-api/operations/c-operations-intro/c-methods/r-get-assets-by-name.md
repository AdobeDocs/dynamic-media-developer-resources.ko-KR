---
description: 에셋 이름의 배열을 기반으로 에셋을 반환합니다.
solution: Experience Manager
title: getAssetsByName
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e48574e3-9d16-45fb-b4c8-98b5e092e611
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 11%

---

# getAssetsByName{#getassetsbyname}

에셋 이름의 배열을 기반으로 에셋을 반환합니다.

구문

## 승인된 사용자 유형 {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자가 읽기 액세스 권한이 있는 자산만 반환합니다.

## 매개 변수 {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**입력(getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> company핸들</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 회사 손잡이. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUser핸들</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 다른 사용자로 액세스를 제공합니다. 관리자만 사용할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 액세스 그룹 핸들</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 특정 그룹별로 필터링하는 데 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 검색할 자산 이름의 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 검색된 자산에 허용된 자산 유형 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 검색된 자산에 대해 제외된 자산 유형 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 검색된 자산에 허용된 자산 하위 유형 배열. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:부울</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>If <span class="codeph"> true</span> 및 <span class="codeph"> assetSubTypeArray</span> 은(는) 비어 있지 않으며 하위 유형이 있는 자산만 표시됩니다. <span class="codeph"> assetSubTypeArray</span> 반환됩니다. </p> <p>If <span class="codeph"> false</span>를 입력하면 정의된 하위 유형이 없는 에셋이 포함됩니다. </p> <p>기본값은 입니다. <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 응답에 포함된 필드 및 하위 필드 목록을 포함합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exclude필드 배열</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 응답에서 제외된 필드 및 하위 필드 목록을 포함합니다. </td> 
  </tr> 
 </tbody> 
</table>

**출력(getAssetsByNameReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetArray | `types:AssetArray` | 아니요 | 필터 조건과 일치하는 에셋의 배열입니다. |

## 예제 {#section-3b7447398e574c88aeaf8ca159cc78dd}

이 코드 샘플은 두 개의 이미지 유형 자산을 반환합니다.

**요청**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**응답**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```
