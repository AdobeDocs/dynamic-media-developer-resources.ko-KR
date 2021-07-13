---
description: 캐시 클러스터링에 이러한 서버 설정을 사용합니다.
solution: Experience Manager
title: 캐시 클러스터링
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# 캐시 클러스터링{#cache-clustering}

캐시 클러스터링에 이러한 서버 설정을 사용합니다.

## PS::cacheCluster.hosts - 호스트 {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

세미콜론으로 구분되는 IP 주소 목록입니다. 이 호스트가 캐시 데이터를 얻을 모든 피어 서버의 IP 주소를 포함하십시오. 편의를 위해 로컬 호스트의 IP 주소를 포함할 수 있다. 이렇게 하면 클러스터의 모든 서버에 대해 동일한 구성 설정이 허용됩니다.

## PS::cacheCluster.updateLocalCache - 로컬 캐시 업데이트 {#section-154c2c0af4544200a3499232bb130dde}

피어 서버에서 제공하는 캐시 항목을 로컬 응답 캐시에 복사해야 하는 경우 &#39;예&#39;로 설정합니다.

## PS::cacheCluster.queryTimeout - 쿼리 시간 초과 {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

피어 서버에서 캐시 항목을 요청할 때 서버는 한 서버가 이 특정 데이터 항목이 있다고 응답하거나 모든 피어 서버가 데이터 항목이 없다는 응답을 받을 때까지 또는 이 설정을 사용하여 지정한 시간(msec)이 만료될 때까지 기다립니다.

## PS::cacheCluster.fetchTimeout - 가져오기 시간 초과 {#section-41c42a29a26f43dc9cff50ad9fae1f14}

서버가 피어 서버에서 실제 캐시 데이터가 전달될 때까지 대기하는 최대 밀리초 수를 지정합니다. 시간 제한이 만료되기 전에 전체 데이터가 전달되지 않은 경우 서버는 피어를 사용할 수 없게 된다고 가정합니다. 그런 다음 캐시 항목이 로컬로 생성됩니다.
