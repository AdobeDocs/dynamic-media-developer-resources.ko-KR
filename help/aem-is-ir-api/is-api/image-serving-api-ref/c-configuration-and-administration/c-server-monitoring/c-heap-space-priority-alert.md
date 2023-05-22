---
description: Java 가비지 수집 주기 직후 사용 가능한 Java 힙 공간이 지정된 임계값 아래에 있는 경우 우선 순위 경고가 전송됩니다.
solution: Experience Manager
title: 힙 공간 우선 순위 경고
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# 힙 공간 우선 순위 경고{#heap-space-priority-alert}

Java 가비지 수집 주기 직후 사용 가능한 Java 힙 공간이 지정된 임계값 아래에 있는 경우 우선 순위 경고가 전송됩니다.

반복되는 경고는 Java 힙 공간을 늘려 해결해야 합니다. 이 조건이 다음에 발생해도 지정된 지연 기간까지 이메일 경고가 발생하지 않습니다. `AS::monitorAlertGenerator.heapSpaceResetInterval` 이(가) 만료되었습니다.
