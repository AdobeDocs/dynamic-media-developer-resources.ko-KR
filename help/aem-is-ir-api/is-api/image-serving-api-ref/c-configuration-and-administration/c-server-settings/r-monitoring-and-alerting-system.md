---
description: 이러한 서버 설정을 사용하여 모니터링 및 경고 시스템을 구성합니다.
solution: Experience Manager
title: 모니터링 및 경고 시스템
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# 모니터링 및 경고 시스템{#monitoring-and-alerting-system}

이러한 서버 설정을 사용하여 모니터링 및 경고 시스템을 구성합니다.

## AS::monitorAlertGenerator.enableGlobalAlerting - 경고 시스템 활성화 {#section-612f8ea61794426ab205e22e5f665fa9}

&#39;true&#39;로 설정하고 이메일 알림 설정을 구성하여 이메일 알림을 활성화합니다. `false`으로 설정하면 모든 이메일 경고가 해제됩니다. 이 기능은 유지 관리를 위해 서버를 오프라인으로 전환할 때 유용합니다. 부울.

## AS::mailSender.host - SMTP 호스트 {#section-151df07e7b44446581339bb7abeeba7a}

SMTP 전자 메일 서버의 IP 주소입니다.

## AS::mailSender.port- SMTP 포트 {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP 전자 메일 서버의 수신 포트입니다.

## AS::monitorAlertGenerator.messageTo - 메시지 수신자 {#section-0017bbaa15434117a70900c3f1163960}

경고를 전송해야 하는 하나 이상의 이메일 주소입니다. 세미콜론을 구분 기호로 사용합니다.

## AS::monitorAlertGenerator.messageFrom - 메시지 보낸 사람 {#section-db320cba4ac2438ca1cfe6abce4aed87}

**[!UICONTROL 보낸 사람]** 이메일 필드에서 사용해야 하는 이메일 주소입니다.

## AS::monitorAlertGenerator.alertInterval - 모니터링 간격 {#section-99cb2e3380c1499e9d5aec3671ed73c7}

모니터링 시스템은 경고 간격 동안 경고 조건을 누적하고 각 간격 끝에 누적된 모든 경고를 포함하는 경고 이메일을 보냅니다. 밀리초, 정수 값, 60000 이상 일반적으로 5분 또는 10분으로 설정됩니다.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Heap Space 경고 간격 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

다른 메시지보다 먼저 힙스페이스 경보가 발생한 후 최소 시간입니다. 간격 시간(밀리초)입니다. 정수 값, 0 이상.

## AS::monitorAlertGenerator.minTrafficForAlerts - 경고 사용 최소 트래픽 {#section-8b4db2d6f96642309ca35c49eb3ab230}

초당 요청 수입니다. 트래픽이 이 이 임계값 미만인 경우 응답 시간 및 오류 경고가 표시되지 않습니다. 트래픽 볼륨에 관계없이 응답 시간 및 오류 경고를 전송하려면 0으로 설정합니다. 실제 값 0 이상
