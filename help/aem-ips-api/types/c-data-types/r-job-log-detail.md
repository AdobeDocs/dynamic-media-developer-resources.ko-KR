---
description: 작업 로그 정보.
seo-description: 작업 로그 정보.
seo-title: 작업 로그 세부 사항
solution: Experience Manager
title: 작업 로그 세부 사항
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---


# JobLogDetail{#joblogdetail}

작업 로그 정보.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 작업 로그의 메시지입니다. |
| `*`logType`*` | `xsd:string` | 작업 로그 파일 유형입니다. |
| `*`assetName`*` | `xsd:string` | 작업 로그의 자산 이름(선택 사항). |
| `*`assetType`*` | `xsd:string` | 자산 유형 선택. |
| `*`assetHandle`*` | `xsd:string` | 작업 로그에서 참조되는 자산 핸들. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | 위에서 설명한 5가지 작업 로그 유형 이외의 추가 작업 로그 정보를 제공합니다. |

