---
description: 모든 로그 파일은 TC 디렉토리에 지정된 동일한 로그 폴더에 기록됩니다.
solution: Experience Manager
title: 서버 로깅
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# 서버 로깅{#server-logging}

모든 로그 파일은 TC::directory로 지정된 동일한 로그 폴더에 기록됩니다.

로그 파일은 일반적으로 매일 만들고 회전합니다. 로그 폴더의 이전 로그 파일은 지정된 일 수( `TC::maxDays`) 후에 자동으로 삭제됩니다.

중요 디스크 공간이 부족하지 않도록 로그 파일에 충분한 디스크 공간을 예약해야 합니다. 많이 사용되는 서버 및 기본 로그 설정에 대해 하루에 1-2GB가 필요할 수 있습니다.

플랫폼 서버 및 이미지 서버는 아래 설명된 3가지 유형의 로그 파일을 만듭니다.

다른 이미지 제공 구성 요소 및 Dynamic Media 뷰어 같은 기타 특정 Dynamic Media 패키지도 동일한 폴더에 로그 파일을 만들 수 있습니다. 이러한 로그 파일은 Dynamic Media 내부용으로 작성된 것으로, 문제 해결을 위해 Dynamic Media 기술 지원에 요청할 수 있습니다.

* [액세스 로그](c-access-log.md)
* [추적 로그](c-trace-log.md)
* [이미지 서버 로그](c-image-server-log.md)

## 참조 {#section-5ff5e46031b1461c92de24e632610d6d}

[액세스 로깅](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f),  [디버그/추적 로깅](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
