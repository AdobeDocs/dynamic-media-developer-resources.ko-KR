---
description: searchAssets 작업에 대한 시스템 필드 검색 조건.
seo-description: searchAssets 작업에 대한 시스템 필드 검색 조건.
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
topic: Dynamic Media Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---


# SystemFieldCondition{#systemfieldcondition}

searchAssets 작업에 대한 시스템 필드 검색 조건.

1차 비교의 경우 시스템 필드 유형에 따라 정확하게 하나의 값( `boolVal`, `longVal`, `doubleVal` 또는 `dateVal`)을 전달합니다. 검색 범위의 경우 `min<Type>` 및 `max<Type>` 매개 변수를 전달하고 `Between` 또는 `NotBetween`의 `op` 값을 전달합니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`필드`*` | `xsd:string` | 자산 검색 시스템 필드 선택. |
| `*`op`*` | `xsd:string` | 문자열 비교 연산자 선택 |
| `*`value`*` | `xsd:string` | 테스트할 값입니다. |
| `*`boolVal`*` | `xsd:boolean` | 부울 비교 값입니다. |
| `*`longVal`*` | `xsd:long` | 긴 비교 값. |
| `*`minLong`*` | `xsd:long` | 긴 범위의 아래쪽 경계. |
| `*`maxLong`*` | `xsd:long` | 긴 범위의 위쪽 경계. |
| `*`doubleVal`*` | `xsd:double` | 이중 비교 값. |
| `*`minDouble`*` | `xsd:double` | 이중 범위의 아래쪽 경계. |
| `*`maxDouble`*` | `xsd:double` | 이중 범위의 위쪽 경계. |
| `*`dateVal`*` | `xsd:dateTime` | 날짜 비교 값입니다. |
| `*`minDate`*` | `xsd:dateTime` | 날짜 범위 미니um. |
| `*`maxDate`*` | `xsd:dateTime` | 최대 날짜 범위. |

## 예 {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

