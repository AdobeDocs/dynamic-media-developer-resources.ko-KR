---
description: 캐시 클러스터링을 위해 이러한 서버 설정을 사용합니다.
seo-description: 캐시 클러스터링을 위해 이러한 서버 설정을 사용합니다.
seo-title: 캐시 클러스터링
solution: Experience Manager
title: 캐시 클러스터링
topic: Scene7 Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# 캐시 클러스터링{#cache-clustering}

캐시 클러스터링을 위해 이러한 서버 설정을 사용합니다.

## PS::cacheCluster.hosts - 호스트 {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

세미콜론으로 구분된 IP 주소 목록. 이 호스트가 캐시 데이터를 얻어야 하는 모든 피어 서버의 IP 주소를 포함합니다. 편의를 위해 로컬 호스트의 IP 주소를 포함할 수 있습니다.이렇게 하면 클러스터의 모든 서버에 대해 동일한 구성 설정을 사용할 수 있습니다.

## PS::cacheCluster.updateLocalCache - 로컬 캐시 업데이트 {#section-154c2c0af4544200a3499232bb130dde}

피어 서버에서 제공한 캐시 항목을 로컬 응답 캐시에 복사해야 하는 경우 &#39;예&#39;로 설정합니다.

## PS::cacheCluster.queryTimeout - 쿼리 시간 초과 {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

피어 서버에서 캐시 항목을 요청할 때 서버는 한 서버가 이 특정 데이터 항목이 있다고 응답하거나 모든 피어 서버에서 데이터 항목이 없다고 응답할 때까지 또는 이 설정으로 지정된 시간(msec)이 만료될 때까지 기다립니다.

## PS::cacheCluster.fetchTimeout - 가져오기 시간 초과 {#section-41c42a29a26f43dc9cff50ad9fae1f14}

서버가 피어 서버에서 실제 캐시 데이터가 배달될 때까지 기다릴 최대 밀리초 수를 지정합니다. 시간 초과가 만료되기 전에 전체 데이터가 배달되지 않은 경우 서버는 피어를 사용할 수 없다고 가정합니다. 그런 다음 캐시 항목이 로컬로 생성됩니다.
