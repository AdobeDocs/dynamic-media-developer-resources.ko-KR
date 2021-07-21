---
description: 요청이 캐시할 수 없는 것으로 표시되지 않는 경우 Platform Server는 모든 회신 이미지와 특정 텍스트 데이터를 디스크에 캐시합니다.
solution: Experience Manager
title: 응답 데이터 캐시
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 응답 데이터 캐시{#response-data-cache}

요청이 캐시할 수 없는 것으로 표시되지 않는 경우 Platform Server는 모든 회신 이미지와 특정 텍스트 데이터를 디스크에 캐시합니다.

Platform Server의 디스크 캐시 위치는 `PS::cache.rootPaths`으로 설정됩니다.

캐시 적중률이 높은 애플리케이션의 경우 여러 디스크 장치 간에 응답 데이터 캐시를 분산하여 서버 성능과 용량을 늘릴 수 있습니다. 각 디스크에 캐시 루트 폴더를 만들어 `PS::cache.rootPaths`에 등록하면 됩니다.

`PS::cache.maxSize` 파일 시스템 오버헤드를 고려하지 않고 모든 캐시 항목의 총 크기를 지정합니다. 실제로 필요한 디스크 공간의 양은 디스크 블록 크기 및 캐시 항목 수와 같은 파일 시스템 속성에 따라 다릅니다. HTTP 디스크 캐시에 대한 디스크 공간은 `PS::cache.maxSize`에 지정된 양보다 두 배 정도 예약하는 것이 좋습니다. 가장 최근에 사용한 알고리즘은 캐시된 데이터의 양을 제한 내에 유지하는 데 사용됩니다.

`PS::cache.maxSize` 외에도 `PS::cache.maxEntries`을 사용하여 최대 캐시 항목 수를 제한하여 응답 캐시를 관리합니다. Linux에서 이 설정은 캐시 파티션에서 사용 가능한 정보 수보다 큰 값을 지정해야 합니다.

>[!NOTE]
>
>Platform Server는 메모리 내 캐시 인덱스를 유지 관리합니다. 이 인덱스의 크기는 `PS::cache.maxEntries` 값의 32바이트입니다. 더 큰 캐시를 수용하려면 Platform Server 힙의 크기를 늘려야 할 수도 있습니다.

시스템이 서버가 순서대로 종료될 때 디스크에 저장된 캐시 인덱스 파일을 사용합니다. 전원 장애 등의 예기치 않은 이벤트가 발생하면 이 파일이 저장되지 않을 수 있습니다. 또한 Platform Server가 준비되려면 몇 분 정도 걸릴 수 있습니다.
