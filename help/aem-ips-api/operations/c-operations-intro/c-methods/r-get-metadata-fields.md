---
description: 자산과 연결된 사용자 정의 메타데이터 필드를 가져옵니다.
seo-description: 자산과 연결된 사용자 정의 메타데이터 필드를 가져옵니다.
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
topic: Scene7 Image Production System API
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getMetadataFields{#getmetadatafields}

자산과 연결된 사용자 정의 메타데이터 필드를 가져옵니다.

구문

## 인증된 사용자 유형 {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-bac949e59c0546429c5786fe422d750d}

**입력(getMetadataFieldsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 담당입니다. |
| ` *`assetType`*` | `xsd:string` | 예 | 메타데이터를 가져올 자산 유형. |

**출력(getMetadataFieldsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`코드 구문`*` | `Code Phrase` |  |  |

## 예제 {#section-dbfde1483d614b5aac2b491cb32115d7}

이 코드 샘플은 지정된 형식 및 회사에 대한 메타데이터 자산을 반환합니다. 응답에는 필드 배열에 메타데이터 필드의 배열이 포함됩니다. 모든 자산에 동일한 메타데이터가 있는 것은 아닙니다. IPS 사용자는 자산의 메타데이터 필드를 정의합니다.

**요청**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**응답**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

