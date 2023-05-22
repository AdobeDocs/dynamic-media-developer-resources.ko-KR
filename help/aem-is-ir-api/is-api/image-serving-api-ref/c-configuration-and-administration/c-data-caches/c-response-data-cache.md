---
description: 다음 [!DNL Platform Server] 요청이 캐시 불가로 표시되지 않는 한 모든 응답 이미지 및 특정 텍스트 데이터를 디스크에 캐시합니다.
solution: Experience Manager
title: 응답 데이터 캐시
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 응답 데이터 캐시{#response-data-cache}

다음 [!DNL Platform Server] 요청이 캐시 불가로 표시되지 않는 한 모든 응답 이미지 및 특정 텍스트 데이터를 디스크에 캐시합니다.

의 위치 [!DNL Platform Server]의 디스크 캐시가 다음으로 설정됨 `PS::cache.rootPaths`.

캐시 적중률이 높은 애플리케이션의 경우 응답 데이터 캐시를 여러 디스크 장치에 분산하여 서버 성능과 용량을 향상시킬 수 있습니다. 각 디스크에 캐시 루트 폴더를 만들어 다음 위치에 등록하면 됩니다 `PS::cache.rootPaths`.

`PS::cache.maxSize` 파일 시스템 오버헤드를 고려하지 않고 모든 캐시 항목의 총 크기를 지정합니다. 실제로 필요한 디스크 공간의 양은 파일 시스템 속성(예: 디스크 블록 크기 및 캐시 항목 수)에 따라 다릅니다. HTTP 디스크 캐시에 대해 디스크 공간을 두 배로 예약하는 것이 좋습니다. `PS::cache.maxSize`. 캐시된 데이터의 양을 제한 내에 유지하기 위해 가장 최근에 사용되지 않는 알고리즘이 사용됩니다.

에 더하여 `PS::cache.maxSize`를 사용하는 최대 캐시 항목 수를 제한하여 응답 캐시를 관리합니다. `PS::cache.maxEntries`. Linux에서 이 설정은 캐시 파티션에서 사용 가능한 inode 수보다 크지 않은 값을 지정해야 합니다.

>[!NOTE]
>
>다음 [!DNL Platform Server] 메모리 내 캐시 인덱스를 유지 관리합니다. 이 인덱스의 크기는 값의 32바이트입니다. `PS::cache.maxEntries`. 을(를) 늘려야 할 수 있습니다. [!DNL Platform Server] 더 큰 캐시를 수용하기 위한 힙 크기입니다.

시스템은 서버가 순서대로 종료될 때 디스크에 저장되는 캐시 인덱스 파일을 사용합니다. 정전 같은 예상치 못한 이벤트가 발생할 경우 이 파일을 저장하지 못할 수 있습니다. 또한 다음 작업을 수행하는 데 몇 분 정도 걸릴 수 있습니다. [!DNL Platform Server] 준비되기 위해.
