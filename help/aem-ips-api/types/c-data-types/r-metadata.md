---
description: searchAssets가 반환하는 메타데이터 필드입니다.
solution: Experience Manager
title: 메타데이터
feature: Dynamic Media Classic,SDK/API,메타데이터
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 12%

---


# 메타데이터{#metadata}

searchAssets가 반환하는 메타데이터 필드입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`name`*` | `xsd:string` | 메타데이터 이름. |
| `*`value`*` | `xsd:string` | 메타데이터 값. |
| `*`boolVal`*` | `xsd:boolean` | 부울 메타데이터 값(부울 형식의 필드에만 해당). |
| `*`longVal`*` | `xsd:long` | 긴 메타데이터 값(int-typed 필드에만 해당). |
| `*`doubleVal`*` | `xsd:double` | 이중 메타데이터 값(부동 소수점 형식의 필드에만 해당). |
| `*`dateVal`*` | `xsd:dateTime` | 날짜 메타데이터 값(날짜 입력 필드에만 해당). |

