---
title: 응답 데이터 캐시
description: ' [!DNL Platform Server] 은(는) 요청이 캐시할 수 없는 것으로 표시되지 않는 한 모든 응답 이미지와 특정 텍스트 데이터를 디스크에 캐시합니다.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
TQID: 'https://experienceleague.adobe.com/zxZqRHFCMKKDxOBb35IEZWEhTFhknDgCKcYatA6lqGs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# 응답 데이터 캐시{#response-data-cache}

요청이 캐시할 수 없는 것으로 표시되지 않으면 [!DNL Platform Server]이(가) 모든 응답 이미지와 특정 텍스트 데이터를 디스크에 캐시합니다.

[!DNL Platform Server]의 디스크 캐시 위치가 `PS::cache.rootPaths`(으)로 설정되었습니다.

캐시 적중률이 높은 애플리케이션의 경우 응답 데이터 캐시를 여러 디스크 장치에 분산하여 서버 성능과 용량을 향상시킬 수 있습니다. 각 디스크에 캐시 루트 폴더를 만들어 `PS::cache.rootPaths`에 등록하면 됩니다.

`PS::cache.maxSize`은(는) 파일 시스템 오버헤드를 고려하지 않고 모든 캐시 항목의 전체 크기를 지정합니다. 필요한 디스크 공간의 양은 디스크 블록 크기와 캐시 항목 수와 같은 파일 시스템 속성에 따라 다릅니다. HTTP 디스크 캐시에 대한 디스크 공간을 `PS::cache.maxSize`에서 지정한 양보다 두 배 많이 예약합니다. 캐시된 데이터의 양을 제한 내에 유지하기 위해 가장 최근에 사용되지 않는 알고리즘이 사용됩니다.

`PS::cache.maxSize` 외에도 응답 캐시는 `PS::cache.maxEntries`로 최대 캐시 항목 수를 제한하여 관리됩니다. Linux®에서 이 설정은 캐시 파티션의 사용 가능한 노드 수보다 크지 않은 값을 지정해야 합니다.

>[!NOTE]
>
>[!DNL Platform Server]이(가) 메모리 내 캐시 인덱스를 유지 관리합니다. 이 인덱스의 크기는 `PS::cache.maxEntries` 값의 32바이트입니다. 필요한 경우 더 큰 캐시를 수용하도록 [!DNL Platform Server] 힙 크기를 늘립니다.

시스템은 서버가 순서대로 종료될 때 디스크에 저장되는 캐시 인덱스 파일을 사용합니다. 정전 같은 예기치 않은 이벤트가 발생하면 이 파일이 저장되지 않을 수 있습니다. 또한 [!DNL Platform Server]이(가) 준비되는 데 몇 분 정도 걸릴 수 있습니다.
