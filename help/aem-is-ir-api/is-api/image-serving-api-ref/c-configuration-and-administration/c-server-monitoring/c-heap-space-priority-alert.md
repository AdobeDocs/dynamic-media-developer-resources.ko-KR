---
description: Java 가비지 수집 주기 바로 다음에 사용 가능한 Java 더미 공간이 지정된 임계값 미만이면 우선순위 경고가 전송됩니다.
seo-description: Java 가비지 수집 주기 바로 다음에 사용 가능한 Java 더미 공간이 지정된 임계값 미만이면 우선순위 경고가 전송됩니다.
seo-title: 더미 공간 우선 순위 경고
solution: Experience Manager
title: 더미 공간 우선 순위 경고
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 더미 공간 우선 순위 경고{#heap-space-priority-alert}

Java 가비지 수집 주기 바로 다음에 사용 가능한 Java 더미 공간이 지정된 임계값 미만이면 우선순위 경고가 전송됩니다.

반복된 경고는 Java 더미 공간을 늘려 해결해야 합니다. 이후에 이 조건이 발생하면 지정된 지연 기간이 만료될 때까지 이메일 경고가 표시되지 `AS::monitorAlertGenerator.heapSpaceResetInterval` 않습니다.
