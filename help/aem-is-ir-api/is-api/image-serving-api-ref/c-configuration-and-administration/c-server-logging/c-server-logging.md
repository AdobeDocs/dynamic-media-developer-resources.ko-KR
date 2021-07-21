---
description: 모든 로그 파일은 TC 디렉토리에 지정된 동일한 로그 폴더에 기록됩니다.
solution: Experience Manager
title: 서버 로깅
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# 서버 로깅{#server-logging}

모든 로그 파일은 TC::directory에 지정된 동일한 로그 폴더에 기록됩니다.

로그 파일은 일반적으로 매일 만들어지고 회전합니다. 로그 폴더의 이전 로그 파일은 지정된 일 수( `TC::maxDays`)가 지나면 자동으로 삭제됩니다.

중요 디스크 공간이 부족하지 않도록 로그 파일에 충분한 디스크 공간을 예약해야 합니다. 서버 및 기본 로그 설정이 많이 사용되는 경우 1-2GB/day가 필요할 수 있습니다.

Platform Server 및 Image Server는 아래에 설명된 세 가지 유형의 로그 파일을 만듭니다.

다른 이미지 제공 구성 요소 및 Dynamic Media Viewer와 같은 특정 기타 Dynamic Media 패키지가 동일한 폴더에 로그 파일을 만들 수도 있습니다. 이러한 로그 파일은 Dynamic Media 내부 사용을 위한 것으로, 문제 해결 목적으로 Dynamic Media 기술 지원 팀에서 요청할 수 있습니다.

* [액세스 로그](c-access-log.md)
* [추적 로그](c-trace-log.md)
* [이미지 서버 로그](c-image-server-log.md)

## 참조 {#section-5ff5e46031b1461c92de24e632610d6d}

[액세스 로깅](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f),  [디버그/추적 로깅](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
