---
description: 지정된 회사와 연결된 속성 집합 유형이나 회사를 지정하지 않은 경우 전역 속성 집합 유형을 가져옵니다.
seo-description: 지정된 회사와 연결된 속성 집합 유형이나 회사를 지정하지 않은 경우 전역 속성 집합 유형을 가져옵니다.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Dynamic Media Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 11%

---


# getPropertySetTypes{#getpropertysettypes}

지정된 회사와 연결된 속성 집합 유형이나 회사를 지정하지 않은 경우 전역 속성 집합 유형을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-ac3ed9e036b54ea993f544046ff0e15d}

**입력(getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
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
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4">속성 집합 유형이 연결되어 있는 회사의 핸들입니다. <p>전역 속성 집합 유형을 반환하려면 생략합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(getPropertySetTypesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | 예 | 지정된 회사와 연결된 속성 집합 유형의 배열이나 회사를 지정하지 않은 경우 글로벌 속성 집합 유형입니다. |

## 예제 {#section-280c406a90864409856aee44d4069a52}

**요청**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**응답**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

