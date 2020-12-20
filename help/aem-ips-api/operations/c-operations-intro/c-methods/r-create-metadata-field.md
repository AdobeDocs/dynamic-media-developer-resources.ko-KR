---
description: 관리자가 컨텐츠 관리 시스템 또는 템플릿 작업을 조정할 새 메타데이터 필드를 만들 수 있습니다. 만들어진 메타데이터 필드의 예로는 키워드, 이미지 작성자에 대한 정보 또는 저작권 소유자 정보가 있습니다.
seo-description: 관리자가 컨텐츠 관리 시스템 또는 템플릿 작업을 조정할 새 메타데이터 필드를 만들 수 있습니다. 만들어진 메타데이터 필드의 예로는 키워드, 이미지 작성자에 대한 정보 또는 저작권 소유자 정보가 있습니다.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
topic: Scene7 Image Production System API
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 7%

---


# createMetadataField{#createmetadatafield}

관리자가 컨텐츠 관리 시스템 또는 템플릿 작업을 조정할 새 메타데이터 필드를 만들 수 있습니다. 만들어진 메타데이터 필드의 예로는 키워드, 이미지 작성자에 대한 정보 또는 저작권 소유자 정보가 있습니다.

구문

## 인증된 사용자 유형 {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## 매개 변수 {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**입력(createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 메타데이터 필드가 속하는 회사의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 자산 유형. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 만들고 있는 메타데이터 필드의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4">메타데이터 필드 유형입니다. <p>메타데이터 필드 유형 상수는 사용 가능한 유형을 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>만들 메타데이터 필드의 기본값(예: <span class="codeph"> Scene 7</span>). </p> <p>태그 필드 유형에는 기본값이 지원되지 않으므로 생략해야 합니다. 태그 필드 유형에 비어 있지 않은 기본값이 지정되면 오류가 반환됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> IPS 시스템별 메타데이터를 숨기거나 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>값이 설정될 때 메타데이터 필드가 강제(유효성이 확인됨)되는지 여부를 나타내는 부울 플래그입니다. </p> <p>true로 설정하면 잘못된 값이 <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>에 설정된 경우 오류가 발생합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 선택한 태그가 가리킬 수 있는 열거된 공유 값 집합을 만들 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

**출력(createMetadataFieldReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | 예 | 새 메타데이터 필드의 핸들입니다. |

## 예제 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

이 코드 샘플은 `createMetadataField`이라는 문자열 유형 메타데이터 필드를 만듭니다. 응답에서 새 메타데이터 필드에 대한 핸들을 반환합니다.

**요청**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**응답**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

