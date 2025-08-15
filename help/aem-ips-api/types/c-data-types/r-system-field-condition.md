---
description: searchAssets 작업에 대한 시스템 필드 검색 조건입니다.
solution: Experience Manager
title: 시스템 필드 조건
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

searchAssets 작업에 대한 시스템 필드 검색 조건입니다.

단항 비교의 경우 시스템 필드 형식에 따라 정확히 하나의 값(`boolVal`, `longVal`, `doubleVal` 또는 `dateVal`)을 전달합니다. 검색 범위의 경우 `min<Type>` 및 `max<Type>` 매개 변수를 전달하고 `op` 또는 `Between`의 `NotBetween` 값을 전달합니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 필드 | `xsd:string` | 에셋 검색 시스템 필드 선택. |
| op | `xsd:string` | 문자열 비교 연산자 선택. |
| 값 | `xsd:string` | 테스트할 값입니다. |
| boolVal | `xsd:boolean` | 부울 비교 값. |
| 롱발 | `xsd:long` | 긴 비교 값. |
| minLong | `xsd:long` | 긴 범위의 하단 경계. |
| maxLong | `xsd:long` | 긴 범위의 위쪽 경계. |
| doubleVal | `xsd:double` | 이중 비교 값. |
| minDouble | `xsd:double` | 이중 범위의 하단 경계. |
| maxDouble | `xsd:double` | 이중 범위의 위쪽 경계. |
| dateVal | `xsd:dateTime` | 날짜 비교 값. |
| minDate | `xsd:dateTime` | 날짜 범위 최소값. |
| maxDate | `xsd:dateTime` | 날짜 범위 최대값. |

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
