---
description: 기존 태그 필드의 사전에 새 태그 값을 추가합니다.
solution: Experience Manager
title: addTagFieldValue
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
TQID: 'https://experienceleague.adobe.com/-DA9IYswE5Mfflys-Cn0Gi62OsMU3O1QYIIKYJNq9QU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 12%

---

# addTagFieldValue{#addtagfieldvalues}

기존 태그 필드의 사전에 새 태그 값을 추가합니다.

구문

## 승인된 사용자 유형 {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**입력(addTagFieldValuesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 태그 필드가 포함된 회사의 핸들입니다. |
| 필드 핸들 | `xsd:string` | 예 | 수정할 태그 필드의 핸들입니다. |
| valueArray | `xsd:string` | 예 | 필드의 기존 사전에 추가할 태그 값의 배열입니다. |

**출력(addTagFieldValuesParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-c4049392f1c548f883b8b1f8f167bada}

**요청**

```java {.line-numbers}
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

