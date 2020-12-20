---
description: 자산에 대한 메타데이터 값을 삭제합니다. 메타데이터 삭제 배열을 사용하여 일괄 처리에서 값을 설정합니다.
seo-description: 자산에 대한 메타데이터 값을 삭제합니다. 메타데이터 삭제 배열을 사용하여 일괄 처리에서 값을 설정합니다.
seo-title: deleteAssetMetadata
solution: Experience Manager
title: deleteAssetMetadata
topic: Scene7 Image Production System API
uuid: 2dc783c6-23da-4a94-8780-3c4ec88ff3f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# deleteAssetMetadata{#deleteassetmetadata}

자산에 대한 메타데이터 값을 삭제합니다. 메타데이터 삭제 배열을 사용하여 일괄 처리에서 값을 설정합니다.

구문

## 허가된 사용자 유형 {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 자산에 대한 읽기 및 삭제 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-0eed164e278b456fbdfb7a50727a0416}

**입력(deleteAssetMetadataParam)**

<table id="table_A4438E2FE5F245E5B73F46CD887BE70F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>필수 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>companyHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>폴더가 속하는 회사의 핸들입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>assetHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>삭제할 자산의 핸들입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>metadataDelete </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>자산에서 삭제할 메타데이터. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>deleteArray </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:MetadataDeleteArray</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>자산에서 삭제할 메타데이터 배열입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(deleteAssetMetadataParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-d5657289f5234bb0a613dcf691507958}

MetadataDelete

```java
    <complexType name="MetadataDelete">
        <sequence>
            <element name="fieldHandle" type="xsd:string"/>
        </sequence>
    </complexType>
```

호출 예

```java
<ac:Request id="deleteAssetMetadata">
 <deleteAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
  <companyHandle>c|101</companyHandle>
  <assetHandle>a|202</assetHandle>
  <deleteArray>
   <items>
    <fieldHandle>m|2919|ASSET|UntypedUDFField1395788289789</fieldHandle>
   </items>
  </deleteArray>
 </deleteAssetMetadataParam>
</ac:Request>
```

