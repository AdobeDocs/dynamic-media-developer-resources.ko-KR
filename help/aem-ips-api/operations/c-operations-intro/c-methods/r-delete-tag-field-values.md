---
description: 태그 필드의 사전에서 태그 필드 값을 제거합니다.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
TQID: 'https://experienceleague.adobe.com/SRTriQHWMLXJtkGeS-sCDZE3-1bu1TKNkKjxgESYOi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 11%

---

# deleteTagFieldValues{#deletetagfieldvalues}

태그 필드의 사전에서 태그 필드 값을 제거합니다.

## 승인된 사용자 유형 {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-5db64a6ae238426395bc760b83587260}

**입력(deleteTagFieldValuesParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 태그 필드가 포함된 회사의 핸들입니다. |
| 필드 핸들 | `xsd:string` | 예 | 수정할 태그 필드의 핸들입니다. |
| valueArray | `types:StringArray` | 예 | 필드의 사전에서 삭제할 태그 값의 배열입니다. |

**출력(deleteTagFieldValuesParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

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
