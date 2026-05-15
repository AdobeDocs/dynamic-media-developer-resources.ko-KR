---
description: 시스템의 리소스 및 유형 사용자.
solution: Experience Manager
title: 사용자
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
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
| 기본 역할 | `xsd:string` | 사용자가 속한 각 회사의 사용자에 대한 역할을 설정합니다. 그러나 사용자 역할 `IpsAmin`은(는) 다른 사용자 역할을 재정의합니다. |
| isValid | `xsd:boolean` | 사용자가 유효한지 여부를 결정합니다. |
| passwordExpires | `xsd:dateTime` | 암호 만료 날짜를 설정합니다. |
