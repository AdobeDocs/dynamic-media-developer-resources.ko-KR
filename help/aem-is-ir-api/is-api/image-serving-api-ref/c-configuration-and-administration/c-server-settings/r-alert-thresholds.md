---
description: 이러한 서버 설정을 사용하여 경고 임계값을 구성합니다.
solution: Experience Manager
title: 경고 임계값
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---


# 경고 임계값{#alert-thresholds}

이러한 서버 설정을 사용하여 경고 임계값을 구성합니다.

## AS:monitorAlertGenerator.maxAverageResponseTime -응답 시간 임계값:monitorAlertGenerator.maxAverageResponseTime -응답 시간 {#section-35111039ac6c4a63ba23fc2c828ab726}

샘플링 간격 동안 요청을 처리하는 평균 시간이 여기에서 설정된 임계값을 초과할 때 응답 시간 경고가 표시됩니다. msec로 표시됨;정수 0 이상 작업의 복잡도에 따라 일반적인 값은 100분에서 1000밀리초 사이입니다.

>[!NOTE]
>
>4xx 또는 5xx의 응답 상태로 이어지는 요청은 이 경고에 대해 고려하지 않습니다.

## AS::monitorAlertGenerator.maxErrorRate - 오류 응답률 임계값 AS::monitorAlertGenerator.maxErrorRate - 오류 응답률 {#section-76ba77fd3102419395e0f86719a1f3ec}

샘플링 간격 동안의 총 응답에 대한 HTTP 오류 응답 비율이 지정된 임계값을 초과할 때 오류 경고가 표시됩니다.

0.0에서 1.0 사이의 실제 값. 일반적으로 0.005에서 0.1 사이로 설정됩니다. 오류 경고를 비활성화하려면 1로 설정합니다.

## AS::monitorAlertGenerator.minRequestRate - 낮은 트래픽 임계값 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

현재 샘플링 간격 동안 받은 초당 평균 요청 수가 이 임계값 미만이면 최소 트래픽 경고가 전송됩니다. 이 값을 0으로 설정하여 경고를 비활성화합니다. 초당 요청으로 표현됩니다. 실제 값 0 이상.

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap 공간 임계값 {#section-ce6705045f6842769030ccb1894594cc}

사용 가능한 최소 Java 더미 공간을 지정합니다. 사용 가능한 더미 공간이 이 임계값 미만인 경우 Java 가비지 수집 주기 직후 우선순위 경고가 전송됩니다. Platform Server의 안전한 작업에 50MB가 권장됩니다. 이 값 위에 사용 가능한 더미 공간을 유지하면 가비지 수집 주기 빈도를 줄여 전체 서버 성능을 향상시킬 수 있습니다. 정수 값(바이트, 0 이상).

## AS::monitorAlertGenerator.maxOverlap - 최대 동시 요청 수 {#section-ddc6925bff944758ab19bcc9cf3f2589}

평균 간격 동안 동시에 처리된 요청의 평균 수가 이 임계값을 초과할 때 오버랩 경고가 트리거됩니다. 오버랩이 높으면 가능한 서버 오버로드 조건을 나타낼 수 있습니다.

정수 값 1 이상. 일반적인 범위는 캐시 히트 속도와 요청 복잡성에 따라 20~50입니다.

## AS::monitorAlertGenerator.lockedThreshold - 잠긴 요청 임계값 {#section-012a1c9937d445708380339279c62d80}

요청이 잠긴 것으로 간주되거나 중단되기 전에 요청이 대기되어야 하는 시간(초)을 지정합니다. 평균 간격의 끝에 지정된 기간 이상 하나 이상의 요청이 보류 중인 경우 잠긴 요청 경고가 표시됩니다. 양의 정수 값(밀리초)입니다.

외국 HTTP 서버에서 데이터를 가져오는 복잡한 렌더링 요청 및 요청을 고려하려면 이 값을 최소 30초로 설정하는 것이 좋습니다(이러한 조건이 이 경고에서 감지되지 않는 경우).
