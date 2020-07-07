---
description: 파일을 덮어쓰기 직전에 req=release 명령을 사용하여 서버를 라이브로 하는 동안 비네팅 파일을 교체하거나 삭제할 수 있습니다.
seo-description: 파일을 덮어쓰기 직전에 req=release 명령을 사용하여 서버를 라이브로 하는 동안 비네팅 파일을 교체하거나 삭제할 수 있습니다.
seo-title: 소스 데이터 파일 삭제 또는 바꾸기
solution: Experience Manager
title: 소스 데이터 파일 삭제 또는 바꾸기
topic: Scene7 Image Serving - Image Rendering API
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# 소스 데이터 파일 삭제 또는 바꾸기{#deleting-or-replacing-source-data-files}

파일을 덮어쓰기 직전에 req=release 명령을 사용하여 서버를 라이브로 하는 동안 비네팅 파일을 교체하거나 삭제할 수 있습니다.

>[!NOTE]
>
>Render Server가 데이터 파일에 액세스하는 동안에는 데이터 파일을 교체하거나 삭제할 수 없습니다.

소스 데이터 파일을 삭제하거나 바꾸면 해당 비네팅에 액세스하는 다음 요청이 있을 때까지 Render Server가 파일을 닫게 됩니다. 파일을 많이 사용하는 경우 여러 번 재시도가 필요할 수 있습니다.

다른 데이터 파일을 바꾸려면 렌더링 서버를 중지해야 합니다.

Platform 서버 캐시 항목은 재료 파일 또는 비네팅을 교체할 때 자동으로 무효화됩니다. ICC 프로필 파일을 교체해도 캐시가 무효화되지 않습니다.

파일 교체 시 발생하는 번거로움을 방지하기 위해 교체 파일에 새 이름을 지정하고 해당 카탈로그 항목을 업데이트하는 것이 좋습니다. 따라서 서버가 활성 상태인 동안 모든 데이터 파일을 바꿀 수 있으며 추가 작업 없이 서버 캐시 항목이 자동으로 만료됩니다. 이 방법은 이미지 카탈로그로 관리되는 모든 데이터 파일에 사용할 수 있습니다.
