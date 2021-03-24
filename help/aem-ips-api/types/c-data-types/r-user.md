---
description: 시스템에서 리소스 및 유형의 사용자입니다.
solution: Experience Manager
title: 사용자
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# 사용자{#user}

시스템에서 리소스 및 유형의 사용자입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | 사용자 핸들. |
| `*`firstName`*` | `xsd:string` | 사용자 이름. |
| `*`lastName`*` | `xsd:string` | 사용자 성. |
| `*`이메일`*` | `xsd:string` | 이메일 주소입니다. |
| `*`defaultRole`*` | `xsd:string` | 사용자가 속한 각 회사의 사용자에 대한 역할을 설정합니다. 그러나 사용자 역할 `IpsAmin`은 다른 사용자 역할을 무시합니다. |
| `*`isValid`*` | `xsd:boolean` | 사용자가 유효한지 확인합니다. |
| `*`passwordExpires`*` | `xsd:dateTime` | 암호 만료일을 설정합니다. |

