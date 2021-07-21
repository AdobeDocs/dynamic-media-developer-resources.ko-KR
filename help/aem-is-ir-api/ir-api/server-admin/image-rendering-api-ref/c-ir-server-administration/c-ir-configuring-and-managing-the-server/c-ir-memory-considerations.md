---
description: '이미지 렌더링에서 사용하는 메모리의 양은 광범위하게 다를 수 있으며 실제 서버 로드 및 사용에 따라 매우 달라집니다(예: 몇 개의 비네팅, 여러 개의 비네팅 크기 및 복잡성 등).'
solution: Experience Manager
title: 메모리 고려 사항
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# 메모리 고려 사항{#memory-considerations}

이미지 렌더링에서 사용하는 메모리의 양은 광범위하게 다를 수 있으며 실제 서버 로드 및 사용에 따라 매우 달라집니다(예: 몇 개의 비네팅, 여러 개의 비네팅 크기 및 복잡성 등).

최상의 성능을 위해서는 메모리 페이징(교환)을 피해야 합니다.

이미지 렌더링은 이미지 서버의 메모리 관리를 공유합니다. 이미지 렌더링을 사용할 때는 추가 메모리를 할당해야 합니다. 물리적 메모리의 30~50%가 합리적인 것일 수 있습니다.

이미지 서버 메모리 할당을 변경하는 방법에 대한 자세한 내용은 이미지 제공 설명서 를 참조하십시오(ImageServer::PhysicalMemory).
