---
description: Platform Server는 모든 응답 이미지 및 특정 텍스트 데이터를 디스크에 캐시합니다. 단, 요청이 캐시에 저장되지는 않습니다.
seo-description: Platform Server는 모든 응답 이미지 및 특정 텍스트 데이터를 디스크에 캐시합니다. 단, 요청이 캐시에 저장되지는 않습니다.
seo-title: 응답 데이터 캐시
solution: Experience Manager
title: 응답 데이터 캐시
topic: Scene7 Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 응답 데이터 캐시{#response-data-cache}

Platform Server는 모든 응답 이미지 및 특정 텍스트 데이터를 디스크에 캐시합니다. 단, 요청이 캐시에 저장되지는 않습니다.

플랫폼 서버의 디스크 캐시 위치는 로 설정됩니다 `PS::cache.rootPaths`.

캐시 적중률이 높은 애플리케이션의 경우 여러 디스크 장치에 응답 데이터 캐시를 배포하여 서버 성능과 용량을 늘릴 수 있습니다. 각 디스크에 캐시 루트 폴더를 만들어 에 등록하면 됩니다. `PS::cache.rootPaths`

`PS::cache.maxSize` 파일 시스템 오버헤드를 고려하지 않고 모든 캐시 항목의 전체 크기를 지정합니다. 실제로 필요한 디스크 공간의 크기는 디스크 블록 크기 및 캐시 항목 수와 같은 파일 시스템 속성에 따라 다릅니다. HTTP 디스크 캐시에 대해 지정된 `PS::cache.maxSize`양보다 2배 많은 디스크 공간을 예약하는 것이 좋습니다. 가장 최근에 사용한 알고리즘은 캐시된 데이터의 양을 제한 내에 유지하는 데 사용됩니다.

또한 응답 `PS::cache.maxSize`캐시는 최대 캐시 항목 수를 제한하여 관리됩니다 `PS::cache.maxEntries`. Linux에서 이 설정은 캐시 파티션에서 사용할 수 있는 inodes의 수보다 크지 않은 값을 지정해야 합니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>플랫폼 서버는 메모리 내 캐시 인덱스를 유지합니다. 이 인덱스의 크기는 값이 32바이트입니다 `PS::cache.maxEntries`. 더 큰 캐시를 수용하려면 Platform Server 더미 크기를 늘려야 할 수도 있습니다.

시스템이 서버가 질서 있게 종료될 때 디스크에 저장된 캐시 인덱스 파일을 사용합니다. 전원 오류와 같은 예기치 않은 이벤트의 경우 이 파일이 저장되지 않을 수 있습니다. 또한 플랫폼 서버가 준비되는 데 몇 분 정도 걸릴 수 있습니다.
