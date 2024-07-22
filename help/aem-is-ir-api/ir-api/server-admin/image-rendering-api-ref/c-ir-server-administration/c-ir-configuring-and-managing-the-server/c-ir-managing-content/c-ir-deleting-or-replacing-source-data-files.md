---
description: 비네팅 파일은 서버가 실행되는 동안 파일을 덮어쓰기 직전에 req=release 명령을 사용하여 교체하거나 삭제할 수 있습니다.
solution: Experience Manager
title: 소스 데이터 파일 삭제 또는 바꾸기
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 소스 데이터 파일 삭제 또는 바꾸기{#deleting-or-replacing-source-data-files}

비네팅 파일은 서버가 실행되는 동안 파일을 덮어쓰기 직전에 req=release 명령을 사용하여 교체하거나 삭제할 수 있습니다.

>[!NOTE]
>
>렌더링 서버가 액세스하는 동안에는 데이터 파일을 바꾸거나 삭제할 수 없습니다.

소스 데이터 파일을 삭제하거나 바꾸면 해당 비네팅에 액세스하는 다음 요청이 있을 때까지 렌더링 서버가 파일을 닫기만 합니다. 파일이 많이 사용되는 경우 여러 번 다시 시도해야 할 수 있습니다.

다른 데이터 파일을 바꾸려면 렌더링 서버를 중지해야 합니다.

재질 파일 또는 비네팅을 바꿀 때 [!DNL Platform Server]개의 캐시 항목이 자동으로 무효화됩니다. ICC 프로필 파일을 바꾸어도 캐시가 무효화되지 않습니다.

파일을 바꾸는 과정에서 발생하는 문제를 방지하려면 대체 파일에 새 이름을 지정하고 해당 카탈로그 항목을 업데이트하는 것이 좋습니다. 이렇게 하면 서버가 활성 상태인 동안 데이터 파일을 바꿀 수 있으며 추가 작업 없이 서버 캐시 항목이 자동으로 부실해집니다. 이 방법은 이미지 카탈로그로 관리되는 모든 데이터 파일에 사용할 수 있습니다.
