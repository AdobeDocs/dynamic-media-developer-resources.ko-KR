---
description: 이러한 서버 설정을 사용하여 경고 임계값을 구성합니다.
solution: Experience Manager
title: 경고 임계값
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 경고 임계값{#alert-thresholds}

이러한 서버 설정을 사용하여 경고 임계값을 구성합니다.

## 다음으로: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS:: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

샘플링 간격 동안 요청을 처리하는 평균 시간이 여기에 설정된 임계값을 초과하는 경우 응답 시간 경고가 내보내집니다. 밀리초 단위로 표시되며, 정수 0 이상입니다. 일반적인 값은 작업의 복잡성에 따라 100~1000msec 사이입니다.

>[!NOTE]
>
>4xx 또는 5xx 응답 상태를 초래하는 요청은 이 경고에 대해 고려되지 않습니다.

## AS::monitorAlertGenerator.maxErrorRate - 오류 응답 속도 ThresholdAS::monitorAlertGenerator.maxErrorRate - 오류 응답 속도 {#section-76ba77fd3102419395e0f86719a1f3ec}

샘플링 간격 동안 총 응답에 대한 HTTP 오류 응답의 비율이 지정된 임계값을 초과하는 경우 오류 경고가 발행됩니다.

0.0과 1.0 사이의 실수 값. 일반적으로 0.005와 0.1 사이로 설정됩니다. 오류 경고를 비활성화하려면 1로 설정합니다.

## AS::monitorAlertGenerator.minRequestRate - 낮은 트래픽 임계값 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

현재 샘플링 간격 동안 받은 초당 평균 요청 수가 이 임계값 아래에 도달하면 최소 트래픽 경고가 전송됩니다. 이 값을 0으로 설정하여 경고를 비활성화합니다. 초당 요청으로 표현됩니다. 실수 값 0 이상.

## AS::monitorAlertGenerator.minFreeHeapSpace - 사용 가능한 힙 공간 임계값 {#section-ce6705045f6842769030ccb1894594cc}

사용 가능한 최소 Java 힙 공간을 지정합니다. 사용 가능한 힙 공간이 이 임계값 아래에 있는 경우 Java 가비지 수집 주기 직후 우선 순위 경고가 전송됩니다. 50MB가 권장됩니다. [!DNL Platform Server]. 사용 가능한 힙 공간을 이 값 이상으로 유지하면 가비지 수집 주기의 빈도가 줄어들어 전체 서버 성능이 향상될 수 있습니다. 정수 값(바이트)(0 이상).

## AS::monitorAlertGenerator.maxOverlap - 최대 동시 요청 수 {#section-ddc6925bff944758ab19bcc9cf3f2589}

평균 간격 동안 동시에 처리된 평균 요청 수가 이 임계값을 초과하는 경우 중복 경보가 트리거됩니다. 겹치는 정도가 높으면 가능한 서버 오버로드 조건을 나타낼 수 있습니다.

정수 값 1 이상입니다. 일반적인 범위는 캐시 적중률 및 요청 복잡성에 따라 20~50입니다.

## AS::monitorAlertGenerator.lockedThreshold - 잠긴 요청 임계값 {#section-012a1c9937d445708380339279c62d80}

요청이 잠겼거나 정지된 것으로 간주되기 전에 보류 중이어야 하는 시간(초)을 지정합니다. 평균 간격이 끝날 때 하나 이상의 요청이 지정된 기간보다 오랫동안 보류 중이면 잠금 요청 경고가 발행됩니다. 양의 정수 값(밀리초)입니다.

외부 HTTP 서버에서 데이터를 가져오는 것과 관련된 복잡한 렌더링 요청 및 요청을 처리하려면 이 값을 최소 30초로 설정하는 것이 좋습니다(이러한 조건이 이 경고에서 검색되지 않는 한).
