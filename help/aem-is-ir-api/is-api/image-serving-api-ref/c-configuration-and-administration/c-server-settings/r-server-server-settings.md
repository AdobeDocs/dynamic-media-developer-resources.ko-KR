---
description: 이러한 서버 설정을 사용하여 서버를 구성합니다.
solution: Experience Manager
title: 서버
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 서버{#server}

이러한 서버 설정을 사용하여 서버를 구성합니다.

## SV::ImageServerMode - 이미지 서버 모드 {#section-991b287f2dde4f77a24fc69d5b32cabd}

Linux에서는 32비트 및 64비트 버전의 이미지 서버를 모두 사용할 수 있습니다. 64비트 Linux 서버에 설치된 경우 ImageServer64, 32비트 서버에 설치된 경우 ImageServer32(기본값)를 지정합니다.

>[!NOTE]
>
>64비트 버전의 Image Server는 FlashPix 소스 파일을 지원하지 않습니다.

>[!NOTE]
>
>64비트 모드는 Windows에서 지원되지 않습니다. 전용 `ImageServer32` 지정할 수 있습니다. 그렇지 않으면 이미지 제공이 시작되지 않습니다.

## SV::PsHeapSize - [!DNL Platform Server] 힙크기 {#section-fd83715948764aeda58d6b3a9f9f8be9}

에 대한 Java heap 크기입니다 [!DNL Platform Server]. 기본값은 &quot;입니다. `512m`&quot; (512MB)

## IS::TcpPort, PS::isConnection.port - 이미지 서버 수신 포트 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

간 통신에 사용되는 포트를 지정합니다. [!DNL Platform Server] 및 이미지 서버를 포함합니다. 호스트 시스템에서 달리 사용되지 않는 포트 번호를 지정해야 합니다.

>[!NOTE]
>
>이미지 제공 기능이 올바르게 작동하려면 `IS::TcpPort` 및 `PS::isConnection.port`.

## IS::PhysicalMemory - 이미지 서버 메모리 제한 {#section-85e37aa2ac6e456eb698da716dd3247d}

실제 메모리의 백분율로 표현되는 메모리 내 이미지 데이터의 대략적인 제한. 유효한 범위는 10%~90%입니다. 이미지 서버는 가능한 경우 이미지 메모리의 사용을 지정된 양만큼 제한하려고 합니다. 처리 작업이 많은 경우 일시적으로 제한을 초과할 수 있습니다.

## IS::WorkerThreads - 이미지 서버 작업자 스레드 수 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

이미지 서버가 이미지 데이터를 처리하는 데 사용하는 최대 스레드 수입니다. 기본값은 0이며, 이 경우 이미지 서버에서 스레드 수를 자동으로 최적화할 수 있습니다.

일부 운영 체제에는 높은 컨텍스트 스위칭 오버헤드가 있는 스레딩 모델이 있습니다. 이러한 경우 특정 스레드 수를 선택하면 전체 서버 성능이 향상될 수 있습니다(예: CPU당 스레드 1개). 최적의 설정을 찾는 데 몇 가지 실험이 필요할 수 있습니다. 자세한 내용은 이미지 제공 릴리스 노트 및 운영 체제 설명서를 참조하십시오.

## IS::NumberOfTextServer - 텍스트 서버 인스턴스 수 {#section-971e20a90c1a473598fba738ed95671a}

동시에 활성화할 최대 텍스트 렌더러 수입니다. 0(기본값)은 사용 가능한 CPU 코어 수의 1.5배에 해당합니다.

## IS::TextServerTcpPortRange - 텍스트 서버 통신 포트 {#section-a13465de88ed4df09931e5ba840c1942}

텍스트 서버 통신에 사용할 포트입니다. &#39;-&#39;로 구분되는 첫 번째 및 마지막 포트 번호를 지정합니다.
