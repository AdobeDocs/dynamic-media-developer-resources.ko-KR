---
description: 회사에 대한 핸들과 속성 집합 형식의 이름을 사용하여 속성 집합 형식을 가져옵니다. 이 메서드는 속성 형식뿐만 아니라 형식에 대한 핸들과 함께 형식 구조를 가져옵니다.
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ff9c3d24-577c-4a9c-8820-60c2a33773bc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 11%

---

# getPropertySetType{#getpropertysettype}

회사에 대한 핸들과 속성 집합 형식의 이름을 사용하여 속성 집합 형식을 가져옵니다. 이 메서드는 속성 형식뿐만 아니라 형식에 대한 핸들과 함께 형식 구조를 가져옵니다.

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
| companyHandle | `xsd:string` | 아니요 | 회사의 손잡이입니다. 속성 세트 유형은 여러 회사에 속할 수 있으므로 선택 사항입니다. |
| 이름 | `xsd:string` | 예 | 속성 집합 형식 이름입니다. |

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 유형</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PropertySetType</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4">다음을 포함하는 유형 구조: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">핸들. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">이름 입력. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">속성 유형입니다. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">형식에서 여러 속성 유형을 허용하는지 여부를 나타내는 값입니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 예제 {#section-1b57199415e34a8fa449f864f8895b14}

이 코드 샘플은 속성 집합 형식을 이름별로 반환합니다.

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
