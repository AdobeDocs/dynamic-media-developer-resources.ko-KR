---
description: 이미지 카탈로그 서비스에 이 서버 설정을 사용하십시오.
solution: Experience Manager
title: 이미지 카탈로그 서비스
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
TQID: 'https://experienceleague.adobe.com/Fs2xGD3Dpd8pe5jtto4kPMF0BrJiLNRvdBn8RSPiQjw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 0%

---

# 이미지 카탈로그 서비스{#image-catalog-service}

이미지 카탈로그 서비스에 이 서버 설정을 사용하십시오.

## CS::catalog.rootPath - 이미지 카탈로그 폴더 {#section-02d107f157384b18835f884f24fea3aa}

이미지 카탈로그 폴더의 위치(모든 [!DNL catalog.ini] 파일이 있어야 함)입니다. 절대 파일 경로이거나 *[!DNL install_folder]*&#x200B;에 상대적인 경로일 수 있습니다. 새 기본 카탈로그 파일([!DNL .ini] 파일 접미사)이 검색되거나 기존 기본 카탈로그 파일의 마지막 수정 시간이 변경된 경우 서버에서 이 폴더를 계속 모니터링하고 카탈로그를 로드하거나 다시 로드합니다.

## CS::catalog.cacheRoot - 카탈로그 캐시 폴더 {#section-73e499c3a5974f1aa4251e70272ff503}

카탈로그 시스템 캐시의 루트 폴더입니다. `PS::cache.rootPaths`에 있는 폴더 중 하나와 동일하게 설정할 수 있습니다. 이 설정을 변경하기 전에 폴더를 수동으로 만들어야 합니다.

## CS::catalog.modificationWaitTime - 카탈로그 파일 구문 분석 지연 {#section-7348065bcc124cb68ea947bf1b9b0845}

[!DNL catalog.ini] 파일이 변경된 후 보조 카탈로그 파일이 로드될 때까지 카탈로그 서비스가 대기하는 시간(밀리초)입니다. 이렇게 하면 카탈로그 서비스가 보조 카탈로그 파일을 로드하기 전에 모든 보조 카탈로그 파일이 최신 상태로 유지되도록 하는 데 도움이 됩니다. 정수 값(밀리초)입니다.

## CS::catalog.refreshInterval - 카탈로그 파일 검사 빈도 {#section-517fefc1d8784777a1026abec8630d58}

카탈로그 서비스가 이미지 카탈로그의 변경 사항을 확인하는 빈도입니다. 정수 값(밀리초)입니다.
