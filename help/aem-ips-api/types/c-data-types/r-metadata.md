---
description: searchAssets에서 반환된 메타데이터 필드.
solution: Experience Manager
title: 메타데이터
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# [!DNL Metadata]{#metadata}

searchAssets에서 반환된 메타데이터 필드.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| name | `xsd:string` | 메타데이터 이름. |
| 값 | `xsd:string` | 메타데이터 값. |
| boolVal | `xsd:boolean` | 부울 메타데이터 값(부울 유형 필드만 해당). |
| 롱발 | `xsd:long` | 긴 메타데이터 값(내부 유형 필드에만 해당). |
| doubleVal | `xsd:double` | 이중 메타데이터 값(부동 소수점 형식 필드만 해당). |
| dateVal | `xsd:dateTime` | 날짜 메타데이터 값(날짜 유형 필드에만 해당). |
