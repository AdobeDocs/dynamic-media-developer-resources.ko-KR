---
description: Java 가비지 수집 주기 직후 사용 가능한 Java 힙이 지정된 임계값 미만인 경우 우선순위 경고가 전송됩니다.
solution: Experience Manager
title: 힙스페이스 우선 순위 경고
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# 힙스페이스 우선 순위 경고{#heap-space-priority-alert}

Java 가비지 수집 주기 직후 사용 가능한 Java 힙이 지정된 임계값 미만인 경우 우선순위 경고가 전송됩니다.

반복된 경고는 Java heap 공간을 늘려 해결해야 합니다. 이 조건이 추가로 발생할 경우 `AS::monitorAlertGenerator.heapSpaceResetInterval`에 지정된 지연 기간이 만료될 때까지 이메일 경고가 발생하지 않습니다.
