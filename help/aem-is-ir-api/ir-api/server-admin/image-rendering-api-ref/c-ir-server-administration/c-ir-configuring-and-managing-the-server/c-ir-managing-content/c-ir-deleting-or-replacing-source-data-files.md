---
description: 파일을 덮어쓰기하기 바로 전에 req=release 명령을 사용하여 서버가 실행되는 동안 비네팅 파일을 교체하거나 삭제할 수 있습니다.
solution: Experience Manager
title: 소스 데이터 파일 삭제 또는 바꾸기
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 소스 데이터 파일 삭제 또는 바꾸기{#deleting-or-replacing-source-data-files}

파일을 덮어쓰기하기 바로 전에 req=release 명령을 사용하여 서버가 실행되는 동안 비네팅 파일을 교체하거나 삭제할 수 있습니다.

>[!NOTE]
>
>Render Server가 데이터 파일에 액세스하는 동안 데이터 파일을 바꾸거나 삭제해야 합니다.

소스 데이터 파일을 삭제하거나 바꾸면 해당 파일에 액세스하는 다음 요청이 있을 때까지 Render Server가 파일을 닫게 됩니다. 파일이 많이 사용되는 경우 여러 번 다시 시도해야 할 수 있습니다.

다른 데이터 파일을 바꾸려면 렌더링 서버를 중지해야 합니다.

재료 파일 또는 비네팅을 교체한 경우 Platform Server 캐시 항목이 자동으로 무효화됩니다. ICC 프로필 파일을 교체해도 캐시가 무효화되지 않습니다.

파일을 교체하는 과정에서 발생하는 번거로움을 방지하기 위해 교체 파일에 새 이름을 지정하고 해당 카탈로그 항목을 업데이트하는 것이 좋습니다. 이렇게 하면 서버가 활성 상태인 동안 모든 데이터 파일을 바꿀 수 있으므로 추가 개입 없이 서버 캐시 항목이 자동으로 사용되지 않게 됩니다. 이 방법은 이미지 카탈로그로 관리되는 모든 데이터 파일에 사용할 수 있습니다.
