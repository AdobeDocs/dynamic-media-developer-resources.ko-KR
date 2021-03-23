---
description: searchAssets가 반환하는 메타데이터 필드입니다.
seo-description: searchAssets가 반환하는 메타데이터 필드입니다.
seo-title: 메타데이터
solution: Experience Manager
title: 메타데이터
uuid: fb7a0ef8-a16c-41e3-84cf-160602cb284b
feature: Dynamic Media Classic,SDK/API,메타데이터
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
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

