---
description: cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.
solution: Experience Manager
title: 이메일 확인
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# EmailConfirmation{#emailconfirmation}

cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.

구문

## 매개 변수 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | true이면 Dynamic Media CDN으로부터 이메일 확인을 수신하도록 지정된 이메일 목록인 사용자의 웹 서비스 사용자 계정을 포함합니다. |
| `*`ccOthersArray`*` | `types:EmailArray` | Dynamic Media CDN으로부터 확인 알림을 수신하도록 지정된 이메일 주소(최대 5개) 배열입니다. |

