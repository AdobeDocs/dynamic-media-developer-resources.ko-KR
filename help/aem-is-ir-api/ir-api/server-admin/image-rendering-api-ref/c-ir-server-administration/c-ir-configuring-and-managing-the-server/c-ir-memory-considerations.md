---
description: '이미지 렌더링에 사용되는 메모리 양은 널리 달라질 수 있으며 실제 서버 부하 및 사용에 따라 상당히 달라집니다(예: 서로 다른 비네팅이 몇 개, 서로 다른 비네팅의 크기 및 복잡도 등).'
seo-description: '이미지 렌더링에 사용되는 메모리 양은 널리 달라질 수 있으며 실제 서버 부하 및 사용에 따라 상당히 달라집니다(예: 서로 다른 비네팅이 몇 개, 서로 다른 비네팅의 크기 및 복잡도 등).'
seo-title: 메모리 고려 사항
solution: Experience Manager
title: 메모리 고려 사항
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# 메모리 고려 사항{#memory-considerations}

이미지 렌더링에 사용되는 메모리 양은 널리 달라질 수 있으며 실제 서버 부하 및 사용에 따라 상당히 달라집니다(예: 서로 다른 비네팅이 몇 개, 서로 다른 비네팅의 크기 및 복잡도 등).

최상의 성능을 위해서는 메모리 페이징(교환)을 피해야 합니다.

이미지 렌더링은 이미지 서버의 메모리 관리를 공유합니다. 이미지 렌더링을 사용할 때는 추가 메모리를 할당해야 합니다. 30~50%의 물리적 메모리가 적당할 수 있습니다.

이미지 서버 메모리 할당(ImageServer::PhysicalMemory)을 변경하는 방법에 대한 자세한 내용은 이미지 제공 설명서를 참조하십시오.
