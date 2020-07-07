---
description: 이러한 서버 설정을 사용하여 경고 임계값을 구성합니다.
seo-description: 이러한 서버 설정을 사용하여 경고 임계값을 구성합니다.
seo-title: 경고 임계값
solution: Experience Manager
title: 경고 임계값
topic: Scene7 Image Serving - Image Rendering API
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# 경고 임계값{#alert-thresholds}

이러한 서버 설정을 사용하여 경고 임계값을 구성합니다.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS: monitorAlertGenerator.maxAverageResponseTime -응답 시간 {#section-35111039ac6c4a63ba23fc2c828ab726}

샘플링 간격 동안 요청을 처리하는 평균 시간이 여기에서 설정된 임계값을 초과할 때 응답 시간 경고가 전송됩니다. msec; 정수 0 이상 작업의 복잡도에 따라 일반적인 값은 100분에서 1000초 사이입니다.

>[!NOTE]
>
>이 경고에 대해 4xx 또는 5xx의 응답 상태가 발생한 요청은 고려되지 않습니다.

## AS::monitorAlertGenerator.maxErrorRate - 오류 응답률 임계값AS::monitorAlertGenerator.maxErrorRate - 오류 응답률 {#section-76ba77fd3102419395e0f86719a1f3ec}

샘플링 간격 동안의 총 응답에 대한 HTTP 오류 응답의 비율이 지정된 임계값을 초과하는 경우 오류 경고가 표시됩니다.

0.0과 1.0 사이의 실제 값. 일반적으로 0.005와 0.1 사이에 설정됩니다. 오류 경고를 비활성화하려면 1로 설정합니다.

## AS::monitorAlertGenerator.minRequestRate - 낮은 트래픽 임계값 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

현재 샘플링 간격 동안 받은 초당 평균 요청 수가 이 임계값 미만이면 최소 트래픽 경고가 전송됩니다. 이 값을 0으로 설정하여 경고를 비활성화합니다. 초당 요청으로 표현됩니다. 실제 값 0 이상

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap Space 임계값 {#section-ce6705045f6842769030ccb1894594cc}

최소 사용 가능한 Java 더미 공간을 지정합니다. 사용 가능한 더미 공간이 이 임계값 미만이면 Java 가비지 수집 주기 직후에 우선순위 경고가 전송됩니다. Platform 서버의 안전한 작업을 위해 50MB가 권장됩니다. 사용 가능한 힙을 이 값보다 높게 유지하면 가비지 수집 주기 빈도를 줄여 전체 서버 성능을 향상시킬 수 있습니다. 정수 값(바이트, 0 이상)

## AS::monitorAlertGenerator.maxOverlap - 최대 동시 요청 수 {#section-ddc6925bff944758ab19bcc9cf3f2589}

평균 간격 동안 동시에 처리된 요청의 평균 수가 이 임계값을 초과할 때 오버랩 경고가 트리거됩니다. 높은 오버랩은 가능한 서버 오버로드 조건을 나타낼 수 있습니다.

정수 값 1 이상. 일반적인 범위는 캐시 히트 속도와 요청 정확도에 따라 20~50입니다.

## AS::monitorAlertGenerator.lockedThreshold - 잠긴 요청 임계값 {#section-012a1c9937d445708380339279c62d80}

요청이 잠기거나 중단된 것으로 간주되기 전에 요청이 보류 중이어야 하는 시간(초)을 지정합니다. 지정된 기간 이상 평균 간격의 끝에 하나 이상의 요청이 보류 중인 경우 잠긴 요청 경고가 표시됩니다. 양의 정수 값(밀리초)입니다.

외부 HTTP 서버에서 데이터를 얻는 것과 관련된 복잡한 렌더링 요청 및 요청을 고려하려면 이 값을 최소 30초로 설정하는 것이 좋습니다(이러한 조건이 이 경고에서 감지되지 않는 경우).
