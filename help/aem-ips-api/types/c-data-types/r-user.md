---
description: 시스템의 리소스 및 유형 사용자입니다.
solution: Experience Manager
title: 사용자
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# 사용자{#user}

시스템의 리소스 및 유형 사용자입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| userHandle | `xsd:string` | 사용자 핸들. |
| firstName | `xsd:string` | 사용자 이름. |
| lastName | `xsd:string` | 사용자 성. |
| 이메일 | `xsd:string` | 이메일 주소. |
| defaultRole | `xsd:string` | 사용자가 속한 각 회사에서 사용자에 대한 역할을 설정합니다. 하지만 사용자 역할은 `IpsAmin` 다른 사용자 역할을 무시합니다. |
| isValid | `xsd:boolean` | 사용자가 유효한지 확인합니다. |
| passwordExpires | `xsd:dateTime` | 암호 만료 날짜를 설정합니다. |
