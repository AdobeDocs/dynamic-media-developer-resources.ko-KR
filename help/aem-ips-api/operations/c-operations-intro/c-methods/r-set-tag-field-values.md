---
description: 기존 태그 필드에 대한 태그 사전 값을 설정합니다.
seo-description: 기존 태그 필드에 대한 태그 사전 값을 설정합니다.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Dynamic Media Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 14%

---


# setTagFieldValues{#settagfieldvalues}

기존 태그 필드에 대한 태그 사전 값을 설정합니다.

구문

## 인증된 사용자 유형 {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-a05cbee4cb4f44198c414a6b14e69156}

**입력**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`fieldHandle`*` | `xsd:string` | 예 | 태그 필드 핸들입니다. |
| `*`valueArray`*` | `types:StringArray` | 예 | 필드의 기존 사전을 대체하는 태그 값의 배열입니다. 새 값이 기존 값과 일치할 때 자산 연결은 유지됩니다. |

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
