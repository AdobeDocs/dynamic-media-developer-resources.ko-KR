---
description: 지정된 검색어에 대한 메타데이터 인덱스 저장소를 검색합니다. searchAssets 메서드와 같은 자산 데이터를 반환합니다.
seo-description: 지정된 검색어에 대한 메타데이터 인덱스 저장소를 검색합니다. searchAssets 메서드와 같은 자산 데이터를 반환합니다.
seo-title: searchAssetsByMetadata
solution: Experience Manager
title: searchAssetsByMetadata
topic: Scene7 Image Production System API
uuid: f4119ee9-f6d8-49fb-9d8c-bb200951d983
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# searchAssetsByMetadata{#searchassetsbymetadata}

지정된 검색어에 대한 메타데이터 인덱스 저장소를 검색합니다. searchAssets 메서드와 같은 자산 데이터를 반환합니다.

사용자 정의 메타데이터 필드에 대해 검색할 `searchAssetsByMetadata` 수 있는 반면, 해당 필드가 에 지정된 경우 반환되지 않습니다 `responseMetadataArray`. 이 점을 설명하려면 다음 코드 예제를 참조하십시오.

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

이 문제를 해결하려면 검색에서 반환되는 자산의 `fieldHandles` 실행을 사용할 수 `getAssets` 있습니다( [getAssets 참조](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)). 이 방법은 해당 자산에 대한 사용자 정의 필드 값을 가져옵니다. 다음 구문 예를 사용하여 사용자 정의 메타데이터 필드를 검색합니다.

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## 인증된 사용자 유형 {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

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
   <td colname="col1"> <p><span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>회사의 손잡이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 필터 <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>검색 기준을 정의하는 데 도움이 되는 필터입니다. </p> <p>SearchFilter <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> metadataConditionArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>검색 기준을 정의하는 조건입니다. 자세한 내용은 아래를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 응답 <span class="varname"> MetadataArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>자산 요약의 응답에 채울 추가 필드. 필드는 정규화된 형식으로 지정해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 페이지당 <span class="varname"> 레코드</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>응답으로 반환되는 자산의 수입니다. 기본값은 1000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 결과</span> 페이지 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>레코드 PerPage 페이지 크기를 기준으로 반환할 결과 페이지를 <span class="codeph"> 지정합니다</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 정렬 <span class="varname"> 기준</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>선택한 자산 필드별로 정렬합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 정렬 <span class="varname"> 방향</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>정렬 방향 선택 기본값은 오름차순입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(searchAssetsByMetadataReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | 아니요 | 일치 항목 수입니다. |
| ` *`assetArray`*` | `types:AssetArray` | 아니요 | 검색에서 반환되는 자산의 배열입니다. |

## metadataConditionArray 세부 사항 {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

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

`field_handle` 은 메타데이터 검색 키입니다. 도트 표기법을 포함할 수 있습니다. 가능한 값은 다음과 같습니다.

* `asset_id` (접두어 없음)
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
* `created_at` (과 `modified_at` 동일(양식의 날짜:2014년 7월 25일 22시 13분 45초 GMT-0500(CDT)

* `created_by`

**허용되는 연산자**

값은 [!DNL operator] 값을 비교하고 다음을 포함하는 방법을 정의합니다.

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

검색할 `comparison_value` 용어입니다.

## 예제 {#section-53a12b9c023e4e629eddf5719c955ad4}

이 코드 샘플은 다음 메타데이터 조건으로 검색을 수행합니다.

* `name` 필드에 포함된 `1000801`값이 있습니다.

* `dc.rights` 필드는 다음과 `Per Jessen Schmidt`같습니다.

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

