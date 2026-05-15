---
description: Java 가비지 수집 주기 직후 사용 가능한 Java 힙 공간이 지정된 임계값 아래에 있는 경우 우선 순위 경고가 전송됩니다.
solution: Experience Manager
title: 힙 공간 우선 순위 경고
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
TQID: 'https://experienceleague.adobe.com/zCx9aodQa-gcTc0iFuK3N0fJf43EdyCWk8cYIawYPaM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 0%

---

# 힙 공간 우선 순위 경고{#heap-space-priority-alert}

Java 가비지 수집 주기 직후 사용 가능한 Java 힙 공간이 지정된 임계값 아래에 있는 경우 우선 순위 경고가 전송됩니다.

반복되는 경고는 Java 힙 공간을 늘려 해결해야 합니다. 이 조건이 다음에 발생해도 `AS::monitorAlertGenerator.heapSpaceResetInterval`(으)로 지정된 지연 기간이 만료될 때까지 전자 메일 경고가 발생하지 않습니다.
