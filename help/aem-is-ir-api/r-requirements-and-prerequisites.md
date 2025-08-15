---
title: 시스템 요구 사항 및 사전 요구 사항
description: Dynamic Media 이미지 서비스 제공을 사용하기 전에 시스템이 시스템 요구 사항을 충족하는지 확인하십시오.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# 시스템 요구 사항 및 사전 요구 사항{#system-requirements-and-prerequisites}

Dynamic Media 이미지 서비스 제공을 사용하기 전에 시스템이 시스템 요구 사항을 충족하는지 확인하십시오.

## 서버 하드웨어 {#section-f3c14a7bc1b745118602659628df779f}

서버는 다음 하드웨어 요구 사항을 충족해야 합니다.

>[!NOTE]
>
>AMD64 및 Intel® EM64T를 지원하는 프로세서가 장착된 시스템은 일반적으로 NUMA(Non-Uniform Memory Architecture) 플랫폼으로 구성됩니다. 이는 커널이 단일 메모리 노드를 구성하는 것이 아니라 부트 시에 여러 메모리 노드를 구성하는 것을 의미한다. 다중 노드 구성은 다른 노드가 소진되기 전에 하나 이상의 노드에서 메모리 소진을 초래할 수 있다. 메모리 소진이 발생하면 커널은 사용 가능한 메모리가 있더라도 프로세스를 종료하기로 결정할 수 있습니다(예: 이미지 서버 또는 [!DNL Platform Server]). 따라서 Adobe에서는 이러한 시스템을 실행하는 경우 NUMA를 끄는 것이 좋습니다. 커널이 이러한 프로세스를 중지하지 않도록 하려면 `numa=off` 시작 옵션을 사용하십시오.

**Windows**

* Intel Xeon® 또는 AMD® Opteron CPU, 최소 4개 코어
* 최소 1GB의 RAM입니다.
* 스왑 공간은 물리적 메모리(RAM)의 최소 두 배와 같습니다.
* 설치 및 기본 작업을 위해 사용 가능한 하드 디스크 공간 2GB, 소스 이미지, 로그, 데이터 캐시 및 매니페스트 파일에 추가 디스크 공간이 필요합니다.
* 고속 이더넷 네트워크 인터페이스 카드.

**Linux®**

* Intel Xeon® 또는 AMD® Opteron CPU, 최소 4개 코어
* 최소 16GB의 RAM입니다.
* 스와핑이 비활성화되었습니다(권장).
* 설치 및 기본 작업을 위해 사용 가능한 하드 디스크 공간 2GB, 소스 이미지, 로그, 데이터 캐시 및 매니페스트 파일에 추가 디스크 공간이 필요합니다.
* 고속 이더넷 네트워크 인터페이스 카드.

**참고(Linux®):** 이미지 제공이 SELinux를 켠 상태에서는 작동하지 않습니다. 이 옵션은 기본적으로 활성화되어 있습니다. SELinux를 비활성화하려면 [!DNL /etc/selinux/config] 파일을 편집하고 SELinux 값을 다음 위치에서 변경합니다.

`SELINUX=enforcing`

종료

`SELINUX=disabled`

**참고(Linux®):** 서버의 호스트 이름을 IP 주소로 확인할 수 있는지 확인하십시오. 가능하지 않은 경우 다음 예제와 같이 정규화된 호스트 이름과 IP 주소를 [!DNL /etc/hosts]에 추가하십시오.

`<ip address> <fully qualified hostname>`

## 서버 소프트웨어 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media 이미지 제공에는 다음 서버 소프트웨어가 필요합니다.

**Windows**

* Microsoft® Windows Server 2008.
* 64비트 운영 체제.

**Linux®**

* Red Hat® Enterprise 5 또는 CentOS 5.5 이상(최신 수정 패치 포함)
* 64비트 운영 체제.

**참고:** Windows에서 이미지 서비스를 사용하려면 Microsoft® Visual Studio 2010을 설치해야 합니다.
