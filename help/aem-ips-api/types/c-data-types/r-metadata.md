---
description: searchAssets에서 반환되는 메타데이터 필드입니다.
seo-description: searchAssets에서 반환되는 메타데이터 필드입니다.
seo-title: 메타데이터
solution: Experience Manager
title: 메타데이터
topic: Scene7 Image Production System API
uuid: fb7a0ef8-a16c-41e3-84cf-160602cb284b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 메타데이터{#metadata}

searchAssets에서 반환되는 메타데이터 필드입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`name`*` | `xsd:string` | 메타데이터 이름. |
| ` *`value`*` | `xsd:string` | 메타데이터 값. |
| ` *`boolVal`*` | `xsd:boolean` | 부울 메타데이터 값(부울 형식의 필드에만 해당) |
| ` *`longVal`*` | `xsd:long` | 긴 메타데이터 값(int 입력 필드에만 해당). |
| ` *`doubleVal`*` | `xsd:double` | 이중 메타데이터 값(부동 입력 필드에만 해당). |
| ` *`dateVal`*` | `xsd:dateTime` | 날짜 메타데이터 값(날짜 입력 필드에만 해당). |

