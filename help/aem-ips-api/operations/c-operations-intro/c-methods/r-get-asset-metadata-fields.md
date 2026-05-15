---
description: 에셋 유형별로 그룹화된 모든 메타데이터 필드를 반환합니다.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
TQID: 'https://experienceleague.adobe.com/QyDh-64MoS4PmvZGP3iELBrhqs6w8vf3aUBlweOspWU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 20%

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
