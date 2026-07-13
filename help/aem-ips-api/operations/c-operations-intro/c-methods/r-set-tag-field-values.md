---
description: 기존 태그 필드에 대한 태그 사전 값을 설정합니다.
solution: Experience Manager
title: setTagFieldValue
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
TQID: 'https://experienceleague.adobe.com/--ArL0CPejqbpJX-G7Z8zdU97WVXXjGfWc74UmOWSV0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 13%

---

# setTagFieldValue{#settagfieldvalues}

기존 태그 필드에 대한 태그 사전 값을 설정합니다.

구문

## 승인된 사용자 유형 {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-a05cbee4cb4f44198c414a6b14e69156}

**입력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| 필드 핸들 | `xsd:string` | 예 | 태그 필드 핸들입니다. |
| valueArray | `types:StringArray` | 예 | 필드의 기존 사전을 대체하는 태그 값의 배열입니다. 에셋 연결은 새 값이 기존 값과 일치할 때 유지됩니다. |

**출력(setTagFieldValuesReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-b11cafd9bed54ab5836c737cc075c918}

**요청**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**응답**

없음.

