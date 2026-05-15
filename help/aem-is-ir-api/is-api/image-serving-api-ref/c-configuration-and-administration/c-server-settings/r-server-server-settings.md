---
description: 이러한 서버 설정을 사용하여 서버를 구성합니다.
solution: Experience Manager
title: 서버
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
TQID: 'https://experienceleague.adobe.com/403CInOL4425Gv35Njb69WSo-QRyvTuDUZEBtNRsvj0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 357
ht-degree: 0%

---

# 서버{#server}

이러한 서버 설정을 사용하여 서버를 구성합니다.

## SV::ImageServerMode - 이미지 서버 모드 {#section-991b287f2dde4f77a24fc69d5b32cabd}

이미지 서버의 32비트 및 64비트 버전 모두 Linux에서 사용할 수 있습니다. 64비트 Linux 서버에 설치할 경우 ImageServer64를 지정하고 32비트 서버에 설치할 경우 ImageServer32(기본값)를 지정합니다.

>[!NOTE]
>
>64비트 버전의 이미지 서버는 FlashPix 소스 파일을 지원하지 않습니다.

>[!NOTE]
>
>64비트 모드는 Windows에서 지원되지 않습니다. `ImageServer32`만 지정할 수 있습니다. 그렇지 않으면 이미지 제공이 시작되지 않습니다.

## SV::PsHeapSize - [!DNL Platform Server] 힙 크기 {#section-fd83715948764aeda58d6b3a9f9f8be9}

[!DNL Platform Server]에 대한 Java 힙 크기입니다. 기본값은 &quot; `512m`&quot;(512MB)입니다.

## IS::TcpPort, PS::isConnection.port - 이미지 서버 수신 포트 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

[!DNL Platform Server]과(와) 이미지 서버 간의 통신에 사용되는 포트를 지정합니다. 호스트 시스템에서 사용되지 않는 포트 번호를 지정해야 합니다.

>[!NOTE]
>
>이미지 제공이 올바르게 작동하려면 `IS::TcpPort` 및 `PS::isConnection.port`에 대해 동일한 값을 설정해야 합니다.

## IS::PhysicalMemory - 이미지 서버 메모리 제한 {#section-85e37aa2ac6e456eb698da716dd3247d}

메모리 내 이미지 데이터의 대략적인 제한으로, 실제 메모리의 백분율로 표시됩니다. 유효한 범위는 10%에서 90%입니다. 이미지 서버는 가능한 경우 지정된 양만큼 이미지 메모리 사용을 제한하려고 합니다. 대량 처리 활동 중에 일시적으로 제한을 초과할 수 있습니다.

## IS::WorkerThreads - Image Server Worker Threads 수 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

이미지 서버에서 이미지 데이터 처리에 사용하는 최대 스레드 수입니다. 기본값은 0으로, 이미지 서버에서 스레드 수를 자동으로 최적화할 수 있습니다.

일부 운영 체제에는 컨텍스트 전환 오버헤드가 높은 스레딩 모델이 있습니다. 이러한 상황에서 특정 스레드 수(예: CPU당 하나의 스레드)를 선택하면 전체 서버 성능이 향상될 수 있습니다. 최적의 설정을 찾기 위해서는 몇 가지 실험이 필요할 수 있다. 자세한 내용은 이미지 제공 릴리스 노트 및 운영 체제 설명서를 참조하십시오.

## IS::NumberOfTextServers - 텍스트 서버 인스턴스 수 {#section-971e20a90c1a473598fba738ed95671a}

동시에 활성화할 수 있는 최대 텍스트 렌더러 수입니다. 0(기본값)은 사용 가능한 CPU 코어 수의 1.5배에 해당합니다.

## IS::TextServerTcpPortRange - 텍스트 서버 통신 포트 {#section-a13465de88ed4df09931e5ba840c1942}

텍스트 서버 통신에 사용할 포트입니다. &#39;-&#39;로 구분된 첫 번째 및 마지막 포트 번호를 지정합니다.
