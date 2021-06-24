---
description: cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# EmailConfirmation{#emailconfirmation}

cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.

구문

## 매개 변수 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`Originator`*` | `xsd:boolean` | true인 경우에는 Dynamic Media CDN에서 이메일 확인을 받도록 지정된 이메일 목록인 사용자의 웹 서비스 사용자 계정을 포함합니다. |
| `*`ccOthersArray`*` | `types:EmailArray` | Dynamic Media CDN에서 확인 알림을 받도록 지정된 이메일 주소(최대 5개) 배열입니다. |
