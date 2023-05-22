---
description: 시스템의 리소스 및 유형 사용자.
solution: Experience Manager
title: 사용자
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---

# [!DNL User]{#user}

시스템의 리소스 및 유형 사용자.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 사용자 핸들 | `xsd:string` | 사용자 핸들. |
| 이름 | `xsd:string` | 사용자 이름. |
| 성 | `xsd:string` | 사용자 성. |
| 이메일 | `xsd:string` | 이메일 주소. |
| 기본 역할 | `xsd:string` | 사용자가 속한 각 회사의 사용자에 대한 역할을 설정합니다. 그러나 사용자 역할 `IpsAmin` 다른 사용자 역할을 무시합니다. |
| isValid | `xsd:boolean` | 사용자가 유효한지 여부를 결정합니다. |
| passwordExpires | `xsd:dateTime` | 암호 만료 날짜를 설정합니다. |
