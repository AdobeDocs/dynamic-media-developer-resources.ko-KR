---
description: 이러한 서버 설정을 사용하여 모니터링 및 경고 시스템을 구성합니다.
solution: Experience Manager
title: 모니터링 및 경고 시스템
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 모니터링 및 경고 시스템{#monitoring-and-alerting-system}

이러한 서버 설정을 사용하여 모니터링 및 경고 시스템을 구성합니다.

## AS::monitorAlertGenerator.enableGlobalAlerting - 경고 시스템 활성화 {#section-612f8ea61794426ab205e22e5f665fa9}

을 &#39;true&#39;로 설정하고 이메일 알림 설정을 구성하여 이메일 알림을 사용하도록 설정합니다. 을 로 설정 `false` 모든 이메일 경고를 끕니다. 이 기능은 유지 관리를 위해 서버를 오프라인으로 전환할 때 유용할 수 있습니다. 부울.

## AS::mailSender.host - SMTP 호스트 {#section-151df07e7b44446581339bb7abeeba7a}

SMTP 전자 메일 서버의 IP 주소입니다.

## AS::mailSender.port- SMTP 포트 {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP 전자 메일 서버의 수신 포트입니다.

## AS::monitorAlertGenerator.messageTo - 메시지 수신자 {#section-0017bbaa15434117a70900c3f1163960}

경고를 전송해야 하는 하나 이상의 이메일 주소. 세미콜론을 구분 기호로 사용하십시오.

## AS::monitorAlertGenerator.messageFrom - 메시지 발신자 {#section-db320cba4ac2438ca1cfe6abce4aed87}

에 사용해야 하는 이메일 주소 **[!UICONTROL 출처:]** 이메일 필드.

## AS::monitorAlertGenerator.alertInterval - 모니터링 간격 {#section-99cb2e3380c1499e9d5aec3671ed73c7}

모니터링 시스템은 경보 간격 동안 경보 조건을 누적하고 각 간격이 끝날 때 모든 누적된 경보가 포함된 경보 이메일을 전송합니다. 밀리초, 정수 값 또는 60000 이상. 일반적으로 5분 또는 10분으로 설정됩니다.

## AS::monitorAlertGenerator.heapSpaceResetInterval - 힙 공간 경고 간격 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

다른 힙 공간 경고가 발생하기 전 최소 힙 공간 경고 발생 시간. 간격 시간(밀리초)입니다. 정수 값, 0 이상.

## AS::monitorAlertGenerator.minTrafficForAlerts - 경고를 활성화하는 최소 트래픽 {#section-8b4db2d6f96642309ca35c49eb3ab230}

초당 요청 수입니다. 트래픽이 이 임계값 아래로 떨어질 경우 응답 시간 및 오류 경고가 발생하지 않습니다. 트래픽 볼륨에 관계없이 응답 시간 및 오류 경고를 보내려면 0으로 설정합니다. 실수 값 0 이상.
