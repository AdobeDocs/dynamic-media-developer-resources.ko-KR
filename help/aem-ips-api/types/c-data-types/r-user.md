---
description: 시스템의 리소스 및 유형 사용자
seo-description: 시스템의 리소스 및 유형 사용자
seo-title: 사용자
solution: Experience Manager
title: 사용자
topic: Scene7 Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 사용자{#user}

시스템의 리소스 및 유형 사용자

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 사용자 핸들 |
| ` *`firstName`*` | `xsd:string` | 사용자 이름입니다. |
| ` *`lastName`*` | `xsd:string` | 사용자 성. |
| ` *`이메일`*` | `xsd:string` | 이메일 주소. |
| ` *`defaultRole`*` | `xsd:string` | 사용자가 속한 각 회사의 사용자에 대한 역할을 설정합니다. 그러나 사용자 역할은 다른 사용자 역할을 `IpsAmin` 무시합니다. |
| ` *`isValid`*` | `xsd:boolean` | 사용자가 유효한지 확인합니다. |
| ` *`passwordExpires`*` | `xsd:dateTime` | 암호 만료 날짜를 설정합니다. |

