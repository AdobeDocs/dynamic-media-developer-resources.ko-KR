---
description: 고유한 메타데이터 필드 값을 가져옵니다.
solution: Experience Manager
title: getUniqueMetadataValue
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
TQID: 'https://experienceleague.adobe.com/iDDSEPmoOHPlfCBx2wN9AEM4xlwC-s6SAPKVDUd6iEk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 24%

---

# getUniqueMetadataValue{#getuniquemetadatavalues}

고유한 메타데이터 필드 값을 가져옵니다.

구문

## 승인된 사용자 유형 {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-b9d1413811c24566b6d095701f0f66db}

**입력(getUniqueMetadataValuesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| 필드 핸들 | `xsd:string` | 아니요 | 메타데이터 필드에 대한 처리입니다. |

**출력(getUniqueMetadataValuesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 값 | `type:StringArray` |  |  |

## 예제 {#section-440f3bc3e5be436cb6ec26117d05f476}

이 코드 샘플은 필드 핸들을 사용하여 특정 메타데이터 값을 반환합니다.

**요청**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**응답**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

