---
description: 캐시 클러스터링을 사용하면 로드 밸런싱이 적용된 여러 서버가 기본 응답 캐시와 보조 데이터 캐시(중첩된/포함된 요청의 경우)의 캐시 항목을 교환할 수 있으며, 여러 서버에서 동일한 캐시 항목을 생성할 필요가 없으므로 서버 응답성이 크게 향상될 수 있습니다.
solution: Experience Manager
title: 캐시 클러스터링
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
TQID: 'https://experienceleague.adobe.com/J1QtNEy9i67oveb1oS2V6-fagqrrlC30oih8AS1g-N4'
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
source-wordcount: 305
ht-degree: 0%

---

# 캐시 클러스터링{#cache-clustering}

캐시 클러스터링을 사용하면 로드 밸런싱이 적용된 여러 서버가 기본 응답 캐시와 보조 데이터 캐시(중첩된/포함된 요청의 경우)의 캐시 항목을 교환할 수 있으며, 여러 서버에서 동일한 캐시 항목을 생성할 필요가 없으므로 서버 응답성이 크게 향상될 수 있습니다.

구성된 경우 서버가 로컬 캐시에 없는 항목에 대한 요청을 받으면 클러스터의 피어 서버에 연결됩니다. 이미지 서버에 항목을 생성하도록 요청하기 전에 이미 해당 데이터 항목이 있는지 확인합니다.

캐시 클러스터링은 주로 캐시 가능한 콘텐츠가 포함된 애플리케이션에 도움이 됩니다. 처음 배포하는 동안과 새로운 콘텐츠를 사용할 때는 서버 로드를 크게 줄여야 합니다.

시간 초과 및 기타 안전 조치는 하나 이상의 피어 서버가 오프라인일 때에도 시스템이 최대 용량으로 계속 작동하도록 합니다.

캐시 클러스터는 다음 두 가지 기본 구성 중 하나로 작동할 수 있습니다.

* `PS::cacheCluster.updateLocalCache`을(를) 사용하도록 설정하면(기본값) 피어 서버에 있는 모든 캐시 항목이 로컬 캐시에 복사됩니다.

  이 구성은 피어 서버 간의 트래픽을 줄입니다. 또한 클러스터의 모든 서버에 모든 캐시 항목을 복제하는 대신 가장 빠른 응답 시간을 제공합니다. 이는 권장되는 구성입니다.

* `PS::cacheCluster.updateLocalCache`을(를) 사용하지 않도록 설정하면 의 다른 서버 데이터가 로컬 캐시에 복사되지 않습니다.

  이렇게 하면 캐시 데이터에 사용 가능한 디스크 공간이 증가합니다. 그러나 피어 서버 간의 트래픽을 증가시키고 전체 응답 시간을 줄입니다. 낮은 캐시 적중률이 표시되는 경우에만 이 구성을 사용하십시오.
