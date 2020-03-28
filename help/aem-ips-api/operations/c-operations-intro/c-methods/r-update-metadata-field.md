---
description: 필드 메타데이터를 업데이트합니다.
seo-description: 필드 메타데이터를 업데이트합니다.
seo-title: updateMetadataField
solution: Experience Manager
title: updateMetadataField
topic: Scene7 Image Production System API
uuid: 8712b09b-b02a-4fb3-a0ed-084dc48a717a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateMetadataField{#updatemetadatafield}

필드 메타데이터를 업데이트합니다.

구문

## 인증된 사용자 유형 {#section-540e91823fee49a4920ca738f7bfeb99}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-69681ed1ddff437ca1c73f46fe835c96}

**입력(updateMetadataFieldParam)**

<table id="table_65D6EE6C402E4F01819822A855B6BB7F"> 
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
   <td colname="col4"> 회사 핸들 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 메타데이터 필드 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 메타데이터 필드 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> defaultValue <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 메타데이터 필드 값. </td> 
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
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 선택한 태그가 가리킬 수 있는 열거형 공유 값 집합을 만들 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

**출력(updateMetadataFieldReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | 예 | 메타데이터 필드 핸들입니다. |

## 예제 {#section-bb7d93ab6d914ddfa294e08983e589ee}

이 코드 샘플 업데이트는 새 이름과 기본값을 메타데이터 필드에 지정합니다. 응답은 업데이트된 필드에 대한 핸들을 반환합니다.

**요청**

```java
<updateMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
   <name>updateMetadataField</name>
   <defaultValue>Default</defaultValue>
</updateMetadataFieldParam>
```

**응답**

```java
<updateMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|updateMetadataField</fieldHandle>
</updateMetadataFieldReturn>
```

