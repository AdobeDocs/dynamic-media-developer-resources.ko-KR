---
description: 회사에 대한 핸들과 속성 집합 유형의 이름을 사용하여 속성 집합 유형을 가져옵니다. 속성 유형은 물론 유형에 대한 핸들의 형식 구조도 가져옵니다.
seo-description: 회사에 대한 핸들과 속성 집합 유형의 이름을 사용하여 속성 집합 유형을 가져옵니다. 속성 유형은 물론 유형에 대한 핸들의 형식 구조도 가져옵니다.
seo-title: getPropertySetType
solution: Experience Manager
title: getPropertySetType
topic: Scene7 Image Production System API
uuid: 203fa949-a81e-455a-a83e-576b6f65e3af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 8%

---


# getPropertySetType{#getpropertysettype}

회사에 대한 핸들과 속성 집합 유형의 이름을 사용하여 속성 집합 유형을 가져옵니다. 속성 유형은 물론 유형에 대한 핸들의 형식 구조도 가져옵니다.

구문

## 인증된 사용자 유형 {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-c9a53400c44744668bd7915f72d2bf3d}

**입력(getPropertySetTypeParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 아니요 | 회사의 손잡이입니다. 속성 집합 유형은 여러 회사에 속할 수 있으므로 선택 사항입니다. |
| ` *`name`*` | `xsd:string` | 예 | 속성 집합 유형 이름입니다. |

**출력(getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4">다음 항목이 포함된 형식 구조입니다. 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">핸들. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">이름을 입력합니다. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">속성 유형입니다. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">형식에 여러 속성 유형이 허용되는지 여부를 나타내는 값입니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 예제 {#section-1b57199415e34a8fa449f864f8895b14}

이 코드 샘플은 이름별로 속성 집합 유형을 반환합니다.

**요청**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**응답**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```

