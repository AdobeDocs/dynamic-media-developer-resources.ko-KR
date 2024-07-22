---
title: saveMetaField
description: 메타데이터 필드를 만들거나 편집합니다. 메타데이터 필드를 만들려면 선택적 필드 핸들을 생략합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 56a45324-5027-4375-a790-c965f682e4b9
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 8%

---

# saveMetaField{#savemetadatafield}

메타데이터 필드를 만들거나 편집합니다. 메타데이터 필드를 만들려면 선택적 필드 핸들을 생략합니다.

>[!NOTE]
>
>이 메서드는 더 이상 사용되지 않습니다.

## 승인된 사용자 유형 {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-ec6827d485a143f4a059a92b18e40f4e}

**입력(saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 이름 </th> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 필드 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 메타데이터를 저장할 자산 유형 선택. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 필드 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 메타데이터 필드 유형 선택. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 모든 에셋에 대한 필드의 기본값. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> IPS 시스템별 메타데이터를 숨기거나 노출합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname">이(가) 적용됨</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>값이 설정될 때 메타데이터 필드가 적용되는지(유효성 확인) 여부를 나타내는 부울 플래그입니다. </p> <p>true로 설정하면 <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>에 잘못된 값이 설정되면 오류가 발생합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(saveMetadataFieldReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 필드 핸들 | `xsd:string` | 예 | 새 메타데이터 필드 핸들. |

## 예제 {#section-4441c26d1f41466ba972b43dd5189e89}

이 코드 샘플은 Asset Type 및 Metadata Field Types 문자열 상수에 의해 제한된 메타데이터 필드를 만듭니다. `fieldHandle` 요소에 유효한 필드 핸들 값이 있으면 메타데이터 값이 변경되고 요청에 지정한 것과 동일한 필드 핸들을 가져옵니다.

**요청**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**응답**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```
