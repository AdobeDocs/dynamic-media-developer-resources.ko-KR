---
description: 메타데이터 인덱스 저장소에서 지정된 검색어를 검색합니다. searchAssets 메서드와 같은 자산 데이터를 반환합니다.
solution: Experience Manager
title: searchAssetsByMeta
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: a0e01edb-c52b-436d-a166-e24cc6861c49
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 5%

---

# searchAssetsByMeta{#searchassetsbymetadata}

메타데이터 인덱스 저장소에서 지정된 검색어를 검색합니다. searchAssets 메서드와 같은 자산 데이터를 반환합니다.

`searchAssetsByMetadata`에서 사용자 정의 메타데이터 필드를 검색할 수 있지만 해당 필드가 `responseMetadataArray`에 지정된 경우에는 반환되지 않습니다. 이 점을 설명하기 위해 다음 코드 예를 참조하십시오.

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

null 값을 반환합니다.

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

이 문제를 해결하려면 검색에서 반환된 자산의 `fieldHandles`을(를) 사용하여 `getAssets`을(를) 실행할 수 있습니다([getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca) 참조). 이 메서드는 해당 에셋의 사용자 정의 필드 값을 가져옵니다. 다음 구문 예를 사용하여 사용자 정의 메타데이터 필드를 검색할 수 있습니다.

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## 승인된 사용자 유형 {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**입력(searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>회사 손잡이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 필터</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>검색 기준을 정의하는 데 도움이 되는 필터. </p> <p><a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>검색 기준을 정의하는 조건입니다. 자세한 내용은 아래를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>에셋 요약의 응답에 채울 추가 필드입니다. 필드는 정규화된 형식으로 지정해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>응답에서 반환된 에셋 수. 기본값은 1000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p><span class="codeph">개의 recordsPerPage</span> 페이지 크기를 기준으로 반환할 결과 페이지를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 정렬 기준</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>선택한 에셋 필드별로 정렬합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>정렬 방향 선택. 오름차순은 기본값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(searchAssetsByMetadataReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 합계 행 수 | `xsd:int` | 아니요 | 일치 항목 수. |
| assetArray | `types:AssetArray` | 아니요 | 검색에서 반환된 에셋 배열. |

## metadataConditionArray 세부 정보 {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**항목 구조**

`metadataConditionArray` 구조는 다음과 같습니다.

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**값**

`field_handle`은(는) 메타데이터 검색 키입니다. 점 표기법을 포함할 수 있습니다. 가능한 값은 다음과 같습니다.

* `asset_id`(접두사 없음)
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at`(`modified_at`과(와) 동일(양식의 날짜: 2014년 7월 25일 금요일 22:13:45 GMT-0500(CDT))

* `created_by`

**허용된 연산자**

[!DNL operator]은(는) 값을 비교하고 다음을 포함하는 방법을 정의합니다.

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

`comparison_value`은(는) 검색할 용어입니다.

## 예제 {#section-53a12b9c023e4e629eddf5719c955ad4}

이 코드 샘플은 다음 메타데이터 조건으로 검색을 수행합니다.

* `name` 필드에 `1000801`이(가) 포함되어 있습니다.

* `dc.rights` 필드가 `Per Jessen Schmidt`입니다.

**요청**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**응답**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```
