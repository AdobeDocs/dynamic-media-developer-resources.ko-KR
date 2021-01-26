---
description: Java 가비지 수집 주기 바로 다음에 사용 가능한 Java 더미 공간이 지정된 임계값 미만인 경우 우선순위 경고가 전송됩니다.
seo-description: Java 가비지 수집 주기 바로 다음에 사용 가능한 Java 더미 공간이 지정된 임계값 미만인 경우 우선순위 경고가 전송됩니다.
seo-title: 공백 우선 순위 경고
solution: Experience Manager
title: 공백 우선 순위 경고
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# 공백 우선 순위 경고{#heap-space-priority-alert}

Java 가비지 수집 주기 바로 다음에 사용 가능한 Java 더미 공간이 지정된 임계값 미만인 경우 우선순위 경고가 전송됩니다.

반복되는 경고는 Java 더미 공간을 늘려서 해결해야 합니다. 이 조건이 발생하면 `AS::monitorAlertGenerator.heapSpaceResetInterval`으로 지정된 지연 기간이 만료될 때까지 이메일 경고가 발생하지 않습니다.
