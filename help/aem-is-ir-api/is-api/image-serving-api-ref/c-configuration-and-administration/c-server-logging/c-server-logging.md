---
description: 모든 로그 파일은 TC 디렉터리로 지정된 동일한 로그 폴더에 기록됩니다.
solution: Experience Manager
title: 서버 로깅
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
TQID: 'https://experienceleague.adobe.com/9I1gAXWb1Rpuml9WCCVPVC7FrpVazWN79Sk0-bb-tDc'
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
source-wordcount: 170
ht-degree: 1%

---

# 서버 로깅{#server-logging}

모든 로그 파일은 TC::directory로 지정된 동일한 로그 폴더에 기록됩니다.

로그 파일은 일반적으로 매일 작성 및 회전됩니다. 로그 폴더의 이전 로그 파일은 지정된 일 수(`TC::maxDays`) 후에 자동으로 삭제됩니다.

중요 디스크 공간이 부족하지 않도록 로그 파일에 충분한 디스크 공간을 예약해야 합니다. 사용량이 많은 서버와 기본 로그 설정에는 하루 1~2GB가 필요할 수 있습니다.

[!DNL Platform Server] 및 이미지 서버는 아래 설명된 세 가지 유형의 로그 파일을 만듭니다.

다른 이미지 제공 구성 요소와 Dynamic Media 뷰어와 같은 특정 기타 Dynamic Media 패키지도 동일한 폴더에 로그 파일을 만들 수 있습니다. 이러한 로그 파일은 Dynamic Media 내부용이며 문제 해결 목적으로 Dynamic Media 기술 지원에서 요청할 수 있습니다.

* [액세스 로그](c-access-log.md)
* [추적 로그](c-trace-log.md)
* [이미지 서버 로그](c-image-server-log.md)

## 참조 {#section-5ff5e46031b1461c92de24e632610d6d}

[액세스 로깅](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [디버그/추적 로깅](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
