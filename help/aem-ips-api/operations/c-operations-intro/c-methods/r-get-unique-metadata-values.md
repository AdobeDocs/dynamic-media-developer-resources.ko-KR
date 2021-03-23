---
description: 고유한 메타데이터 필드 값을 가져옵니다.
seo-description: 고유한 메타데이터 필드 값을 가져옵니다.
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
feature: Dynamic Media Classic,SDK/API,메타데이터
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 22%

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

