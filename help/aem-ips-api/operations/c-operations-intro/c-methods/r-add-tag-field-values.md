---
description: 기존 태그 필드의 사전에 새 태그 값을 추가합니다.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 13%

---

# addTagFieldValues{#addtagfieldvalues}

기존 태그 필드의 사전에 새 태그 값을 추가합니다.

구문

## 인증된 사용자 유형 {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**입력(addTagFieldValuesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 태그 필드가 포함된 회사의 핸들. |
| `*`fieldHandle`*` | `xsd:string` | 예 | 수정할 태그 필드의 핸들입니다. |
| `*`valueArray`*` | `xsd:string` | 예 | 필드의 기존 사전에 추가할 태그 값의 배열입니다. |

**출력(addTagFieldValuesParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-c4049392f1c548f883b8b1f8f167bada}

**요청**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**응답**

없음.
