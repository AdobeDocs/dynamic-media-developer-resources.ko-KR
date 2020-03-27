---
description: 기존 태그 필드의 사전에 새 태그 값을 추가합니다.
seo-description: 기존 태그 필드의 사전에 새 태그 값을 추가합니다.
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: 9304f02c-a1df-4477-ab33-f2491c390c92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 태그 필드를 포함하는 회사의 핸들 |
| ` *`fieldHandle`*` | `xsd:string` | 예 | 수정할 태그 필드의 핸들 |
| ` *`valueArray`*` | `xsd:string` | 예 | 필드의 기존 사전에 추가할 태그 값의 배열입니다. |

**출력(addTagFieldValuesParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

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
