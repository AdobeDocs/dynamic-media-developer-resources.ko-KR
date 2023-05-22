---
description: 캐시 클러스터링에 이러한 서버 설정을 사용합니다.
solution: Experience Manager
title: 캐시 클러스터링
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# 캐시 클러스터링{#cache-clustering}

캐시 클러스터링에 이러한 서버 설정을 사용합니다.

## PS::cacheCluster.hosts - 호스트 {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

세미콜론으로 구분된 IP 주소 목록. 이 호스트가 캐시 데이터를 가져와야 하는 모든 피어 서버의 IP 주소를 포함합니다. 편의상 로컬 호스트의 IP 주소를 포함할 수 있습니다. 따라서 클러스터의 모든 서버에 대해 동일한 구성 설정을 사용할 수 있습니다.

## PS::cacheCluster.updateLocalCache - 로컬 캐시 업데이트 {#section-154c2c0af4544200a3499232bb130dde}

피어 서버에서 제공한 캐시 항목을 로컬 응답 캐시에 복사해야 하는 경우 &#39;예&#39;로 설정합니다.

## PS::cacheCluster.queryTimeout - 쿼리 시간 초과 {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

피어 서버에서 캐시 항목을 요청할 때 서버는 한 서버가 이 특정 데이터 항목을 가지고 있다고 응답하거나 모든 피어 서버가 데이터 항목을 가지고 있지 않다고 응답하거나 이 설정으로 지정된 시간(밀리초)이 만료될 때까지 기다립니다.

## PS::cacheCluster.fetchTimeout - 가져오기 시간 초과 {#section-41c42a29a26f43dc9cff50ad9fae1f14}

피어 서버에서 실제 캐시 데이터가 전달될 때까지 서버가 대기할 최대 시간(밀리초)을 지정합니다. 제한 시간이 만료되기 전에 전체 데이터가 전달되지 않으면 서버는 피어를 사용할 수 없다고 가정합니다. 그러면 캐시 항목이 로컬로 생성됩니다.
