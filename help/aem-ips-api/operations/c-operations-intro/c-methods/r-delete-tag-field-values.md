---
description: 태그 필드의 사전에서 태그 필드 값을 제거합니다.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 13%

---

# deleteTagFieldValues{#deletetagfieldvalues}

태그 필드의 사전에서 태그 필드 값을 제거합니다.

## 인증된 사용자 유형 {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-5db64a6ae238426395bc760b83587260}

**입력(deleteTagFieldValuesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 태그 필드가 포함된 회사의 핸들. |
| `*`fieldHandle`*` | `xsd:string` | 예 | 수정할 태그 필드의 핸들입니다. |
| `*`valueArray`*` | `types:StringArray` | 예 | 필드의 사전에서 삭제할 태그 값의 배열입니다. |

**출력(deleteTagFieldValuesParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-92f9e575a6da491caa09e264b4d6ee55}

**요청**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**응답**

없음.
