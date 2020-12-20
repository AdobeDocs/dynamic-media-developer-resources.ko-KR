---
description: Scene7 Image Serving을 사용하기 전에 시스템이 시스템 요구 사항을 충족하는지 확인하십시오.
seo-description: Scene7 Image Serving을 사용하기 전에 시스템이 시스템 요구 사항을 충족하는지 확인하십시오.
seo-title: 시스템 요구 사항 및 필수 조건
solution: Experience Manager
title: 시스템 요구 사항 및 필수 조건
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---


# 시스템 요구 사항 및 필수 조건{#system-requirements-and-prerequisites}

Scene7 Image Serving을 사용하기 전에 시스템이 시스템 요구 사항을 충족하는지 확인하십시오.

## 서버 하드웨어 {#section-f3c14a7bc1b745118602659628df779f}

서버는 다음 하드웨어 요구 사항을 충족해야 합니다.

>[!NOTE]
>
>AMD64 및 Intel® EM64T를 지원하는 프로세서가 있는 시스템은 일반적으로 NUMA(Non-Uniform Memory Architecture) 플랫폼으로 구성됩니다. 즉, 커널은 단일 메모리 노드를 구성하지 않고 부팅 시 여러 메모리 노드를 생성합니다. 다중 노드 구문으로 인해 다른 노드가 모두 소진되기 전에 하나 이상의 노드에서 메모리 소모가 발생할 수 있습니다. 메모리 소모가 발생하는 경우 사용 가능한 메모리가 있더라도 커널에서 처리 과정(예: 이미지 서버 또는 플랫폼 서버)을 종료하기로 결정할 수 있습니다. 따라서 Adobe Systems에서는 이러한 시스템을 실행하는 경우 NUMA를 끄는 것이 좋습니다. 커널이 이러한 프로세스를 중지하지 않도록 하려면 `numa=off` 시작 옵션을 사용합니다.

**Windows**

* 4개 이상의 코어가 있는 Intel Xeon® 또는 AMD® Opteron CPU.
* 최소 16GB RAM
* 실제 메모리(RAM)의 최소 두 배만큼 공간을 바꿉니다.
* 설치 및 기본 작업을 위한 2GB의 하드 디스크 여유 공간, 소스 이미지, 로그, 데이터 캐시 및 매니페스트 파일에 추가 디스크 공간이 필요합니다.
* 고속 이더넷 네트워크 인터페이스 카드.

**Linux**

* 4개 이상의 코어가 있는 Intel Xeon® 또는 AMD® Opteron CPU.
* 최소 16GB RAM
* 비활성화된 항목 교환(권장).
* 설치 및 기본 작업을 위한 2GB의 하드 디스크 여유 공간, 소스 이미지, 로그, 데이터 캐시 및 매니페스트 파일에 추가 디스크 공간이 필요합니다.
* 고속 이더넷 네트워크 인터페이스 카드.

**참고(Linux):** 이미지 제공 기능은 SELinux를 켜는 경우 작동하지 않습니다. 이 옵션은 기본적으로 활성화되어 있습니다. SELinux를 비활성화하려면 [!DNL /etc/selinux/config] 파일을 편집하고 SELinux 값을 다음 위치에서 변경합니다.

`SELINUX=enforcing`

to

`SELINUX=disabled`

**참고(Linux):** 서버의 호스트 이름이 IP 주소로 확인될 수 있는지 확인합니다. 허용되지 않는 경우 다음 예와 같이 정규화된 호스트 이름과 IP 주소를 [!DNL /etc/hosts]에 추가하십시오.

`<ip address> <fully qualified hostname>`

## 서버 소프트웨어 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Scene7 이미지 제공에는 다음 서버 소프트웨어가 필요합니다.

**Windows**

* Microsoft® Windows 2008 Server.
* 64비트 운영 체제.

**Linux**

* Red Hat® Enterprise 5 또는 CentOS 5.5 이상, 최신 수정 패치 포함
* 64비트 운영 체제.

**참고:** Windows에서 이미지 제공을 사용하려면 Microsoft Visual Studio 2010 재배포 가능 버전을 설치해야 합니다. 재배포 가능 기간은 다음 위치에서 사용할 수 있습니다.

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

