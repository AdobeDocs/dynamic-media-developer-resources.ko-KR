---
description: 고유한 메타데이터 필드 값을 가져옵니다.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 24%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

고유한 메타데이터 필드 값을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-6a6b67e10a4c4e7bb18306115713380e}

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
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 담당입니다. |
| `*`fieldHandle`*` | `xsd:string` | 아니요 | 메타데이터 필드를 처리합니다. |

**출력(getUniqueMetadataValuesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`values`*` | `type:StringArray` |  |  |

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

