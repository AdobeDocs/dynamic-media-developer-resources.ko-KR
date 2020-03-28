---
description: 메타데이터 필드를 만들거나 편집합니다. 선택적 필드 핸들을 생략하여 새 메타데이터 필드를 만듭니다.
seo-description: 메타데이터 필드를 만들거나 편집합니다. 선택적 필드 핸들을 생략하여 새 메타데이터 필드를 만듭니다.
seo-title: saveMetadataField
solution: Experience Manager
title: saveMetadataField
topic: Scene7 Image Production System API
uuid: ccd84366-732a-4caf-914d-3bc5fe499e7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveMetadataField{#savemetadatafield}

메타데이터 필드를 만들거나 편집합니다. 선택적 필드 핸들을 생략하여 새 메타데이터 필드를 만듭니다.

>[!NOTE]
>
>이 메서드는 더 이상 사용되지 않습니다.

## 인증된 사용자 유형 {#section-0c1cbde0863346f8a31b32fd06ab2926}

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
   <td colname="col1"> <span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 회사의 손잡이입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 필드 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자산 <span class="varname"> 유형</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 메타데이터를 저장할 자산 유형 선택 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 필드 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 필드</span> 유형 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 메타데이터 필드 유형 선택 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> defaultValue <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 모든 자산에 대한 필드의 기본값. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 숨김</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> IPS 시스템별 메타데이터를 숨기거나 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>값이 설정될 때 메타데이터 필드가 강제(유효성 검사)되는지 여부를 나타내는 부울 플래그. </p> <p>true로 설정된 경우 setAssetMetadata /batchSetAssetMetadata에 잘못된 값이 설정되어 있으면 <span class="codeph"> 오류가</span> 발생합니다<span class="codeph"></span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(saveMetadataFieldReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | 예 | 새 메타데이터 필드의 핸들 |

## 예제 {#section-4441c26d1f41466ba972b43dd5189e89}

이 코드 샘플은 자산 유형 및 메타데이터 필드 유형 문자열 상수로 제한된 새 메타데이터 필드를 만듭니다. 요소에 올바른 필드 핸들 값이 있으면 메타데이터 값이 변경되고 요청에 지정한 것과 동일한 필드 핸들이 됩니다. `fieldHandle`

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

