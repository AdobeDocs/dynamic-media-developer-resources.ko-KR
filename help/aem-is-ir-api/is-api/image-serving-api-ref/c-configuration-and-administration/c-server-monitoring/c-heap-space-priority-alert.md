---
description: Java 가비지 수집 주기 바로 다음에 사용 가능한 Java 더미 공간이 지정된 임계값 미만인 경우 우선순위 경고가 전송됩니다.
solution: Experience Manager
title: 공백 우선 순위 경고
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# 공백 우선 순위 경고{#heap-space-priority-alert}

Java 가비지 수집 주기 바로 다음에 사용 가능한 Java 더미 공간이 지정된 임계값 미만인 경우 우선순위 경고가 전송됩니다.

반복되는 경고는 Java 더미 공간을 늘려서 해결해야 합니다. 이 조건이 발생하면 `AS::monitorAlertGenerator.heapSpaceResetInterval`으로 지정된 지연 기간이 만료될 때까지 이메일 경고가 발생하지 않습니다.
