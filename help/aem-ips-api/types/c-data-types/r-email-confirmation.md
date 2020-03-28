---
description: cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.
seo-description: cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.
seo-title: 이메일 확인
solution: Experience Manager
title: 이메일 확인
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 이메일 확인{#emailconfirmation}

cdnCacheInvalidation 작업에 대한 응답으로 지정된 수신자에게 이메일을 보냅니다.

구문

## 매개 변수 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | true인 경우 사용자의 웹 서비스 사용자 계정을 포함합니다. 이 계정은 Scene7 CDN에서 이메일 확인을 받도록 지정된 이메일 목록입니다. |
| ` *`ccOthersArray`*` | `types:EmailArray` | Scene7 CDN에서 확인 알림을 수신하도록 지정된 이메일 주소(최대 5개)의 배열입니다. |

