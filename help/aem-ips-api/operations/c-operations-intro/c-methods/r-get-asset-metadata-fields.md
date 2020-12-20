---
description: 자산 유형별로 그룹화된 모든 메타데이터 필드를 반환합니다.
seo-description: 자산 유형별로 그룹화된 모든 메타데이터 필드를 반환합니다.
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
topic: Scene7 Image Production System API
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 20%

---


# getAssetMetadataFields{#getassetmetadatafields}

자산 유형별로 그룹화된 모든 메타데이터 필드를 반환합니다.

구문

## 인증된 사용자 유형 {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 메타데이터를 검색할 회사의 핸들입니다. |

**출력(getAssetMetadataFieldsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | 예 | 자산 유형별로 메타데이터 필드의 배열입니다. |

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
>간결하게 잘렸습니다.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

