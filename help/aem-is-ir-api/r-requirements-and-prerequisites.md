---
description: Dynamic Media 이미지 제공 기능을 사용하기 전에 시스템이 시스템 요구 사항을 충족하는지 확인하십시오.
solution: Experience Manager
title: 시스템 요구 사항 및 사전 요구 사항
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 시스템 요구 사항 및 사전 요구 사항{#system-requirements-and-prerequisites}

Dynamic Media 이미지 제공 기능을 사용하기 전에 시스템이 시스템 요구 사항을 충족하는지 확인하십시오.

## 서버 하드웨어 {#section-f3c14a7bc1b745118602659628df779f}

서버가 다음 하드웨어 요구 사항을 충족해야 합니다.

>[!NOTE]
>
>AMD64 및 Intel® EM64T을 지원하는 프로세서가 있는 시스템은 일반적으로 NUMA(Non-Uniform Memory Architecture) 플랫폼으로 구성됩니다. 즉, 커널이 단일 메모리 노드를 구성하는 대신 부팅 시 여러 메모리 노드를 구성함을 의미합니다. 다중 노드 구문은 다른 노드가 소진되기 전에 하나 이상의 노드에서 메모리 소진을 일으킬 수 있습니다. 메모리 소모가 발생하면 커널에서 프로세스(예: 이미지 서버 또는 [!DNL Platform Server]) 사용 가능한 메모리가 있어도 따라서 Adobe Systems에서는 이러한 시스템을 실행하는 경우 NUMA를 끄는 것이 좋습니다. 를 사용하십시오 `numa=off` 커널에서 이러한 프로세스를 중지하지 않도록 하려면 시작 옵션을 선택하십시오.

**Windows**

* 4개 이상의 코어가 있는 Intel Xeon® 또는 AMD® Opteron CPU.
* 최소 16GB RAM
* 공간을 실제 메모리(RAM)의 두 배 이상으로 바꿉니다.
* 설치 및 기본 작업을 위한 2GB의 사용 가능한 하드 디스크 공간, 소스 이미지, 로그, 데이터 캐시 및 매니페스트 파일에 추가 디스크 공간이 필요합니다.
* 고속 이더넷 네트워크 인터페이스 카드.

**Linux**

* 4개 이상의 코어가 있는 Intel Xeon® 또는 AMD® Opteron CPU.
* 최소 16GB RAM
* 비활성화된 상태로 교체(권장).
* 설치 및 기본 작업을 위한 2GB의 사용 가능한 하드 디스크 공간, 소스 이미지, 로그, 데이터 캐시 및 매니페스트 파일에 추가 디스크 공간이 필요합니다.
* 고속 이더넷 네트워크 인터페이스 카드.

**참고(Linux):** 이미지 제공이 SELinux를 켜면 작동하지 않습니다. 이 옵션은 기본적으로 활성화되어 있습니다. SELinux를 비활성화하려면 [!DNL /etc/selinux/config] 파일 및 SELinux 값을 다음으로 변경합니다.

`SELINUX=enforcing`

to

`SELINUX=disabled`

**참고(Linux):** 서버의 호스트 이름을 IP 주소로 확인할 수 있는지 확인하십시오. 불가능한 경우 정규화된 호스트 이름과 IP 주소를 [!DNL /etc/hosts] 다음 예와 같습니다.

`<ip address> <fully qualified hostname>`

## 서버 소프트웨어 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media 이미지 서비스에는 다음 서버 소프트웨어가 필요합니다.

**Windows**

* Microsoft® Windows 2008 Server.
* 64비트 운영 체제.

**Linux**

* Red Hat® Enterprise 5 또는 CentOS 5.5 이상(최신 수정 패치 포함)
* 64비트 운영 체제.

**참고:** Windows에서 이미지 제공 서비스를 사용하려면 Microsoft Visual Studio 2010 재배포 가능 패키지를 설치해야 합니다.
