---
description: cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.
solution: Experience Manager
title: 이메일 확인
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.

구문

## 매개 변수 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 이름 | 유형 | 설명 |
|---|---|---|
| 작성자 | `xsd:boolean` | true인 경우 에는 사용자의 웹 서비스 사용자 계정이 포함됩니다. 이 계정은 Dynamic Media CDN에서 이메일 확인을 받도록 지정된 이메일 목록입니다. |
| 기타 배열 | `types:EmailArray` | Dynamic Media CDN에서 확인 알림을 받도록 지정된 이메일 주소 배열(최대 5개)입니다. |
