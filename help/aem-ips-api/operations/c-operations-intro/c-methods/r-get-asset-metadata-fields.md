---
description: 에셋 유형별로 그룹화된 모든 메타데이터 필드를 반환합니다.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 23%

---

# getAssetMetadataFields{#getassetmetadatafields}

에셋 유형별로 그룹화된 모든 메타데이터 필드를 반환합니다.

구문

## 승인된 사용자 유형 {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**입력(getAssetMetadataFieldsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 메타데이터를 검색할 회사에 대한 핸들입니다. |

**출력(getAssetMetadataFieldsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | 예 | 에셋 유형별 메타데이터 필드 배열. |

## 예제 {#section-d79ab85f29144635b0b61416e52f4f3f}

**요청**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**응답**

>[!NOTE]
>
>간결성을 위해 잘립니다.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
