---
description: 이러한 서버 설정을 사용하여 추적 로깅을 디버깅합니다.
seo-description: 이러한 서버 설정을 사용하여 추적 로깅을 디버깅합니다.
seo-title: Debug_trace 로깅
solution: Experience Manager
title: Debug_trace 로깅
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Debug_trace 로깅{#debug-trace-logging}

이러한 서버 설정을 사용하여 추적 로깅을 디버깅합니다.

>[!NOTE]
>
>모든 로그 파일이 동일한 폴더에 작성되도록 구성하는 것이 좋습니다 `TC::directory`. 이렇게 하면 모든 이미지 제공 로그 파일이 로 구성된 자동 로그 파일 순환 `TC::maxDays`에 참여할 수 있으므로 디스크 공간 부족 상황으로 인해 잠재적인 서버 불안정을 방지할 수 있습니다.

## SV::log - 서버 수퍼바이저 추적 로그 파일 경로 {#section-3697bc480ff646e79cacc2812c55ef26}

서버 감독자 로그 파일의 폴더 및 기본 파일 이름입니다. 경로는 절대 경로이거나 상대 경로일 수 있습니다 *[!DNL install_folder]*. 서버 감독자는 파일 이름(파일 접미사 앞에 있는 경우)에 하이픈과 현재 날짜( *[!DNL -yyyy-mm-dd]*)를 추가합니다. Platform 서버()에서 구현한 로그 파일 관리를 활용하려면 모든 로그 파일을 Platform 서버 로그 파일( `PS::LogFolder`)과 동일한 폴더로 보내는 것이 `PS::LogDays`좋습니다. Default is [!DNL logs/Supervisor.log].

>[!NOTE]
>
>이 설정을 변경하기 전에 새 폴더를 만들어야 합니다. 서버 관리자가 필요한 작성, 읽기 및 쓰기 권한을 갖도록 액세스 권한이 설정되어 있는지 확인합니다.

## SV::tracelevel - 서버 수퍼바이저 추적 로그 수준 {#section-36f8634741da4c618d67aa628b5fe474}

로그 수준은 1, 2, 3 또는 4일 수 있습니다. 기본값은 2입니다.

## IS::로그 - 이미지 서버 디버그 로그 파일 경로 {#section-73a3f09b77f2446c9f82207b7d8aec39}

이미지 서버 추적 로그 파일의 폴더 및 기본 파일 이름입니다. 경로는 절대 경로이거나 상대 경로일 수 있습니다 *[!DNL install_folder]*. ImageServer는 파일 이름(있는 경우 파일 접미사 앞)에 하이픈과 현재 날짜( *[!DNL -yyyy-mm-dd]*)를 추가합니다. Platform 서버에서 구현한 로그 파일 관리를 활용하려면 이미지 서버 로그 파일을 Platform 서버 로그 파일( `PS::LogFolder``PS::LogDays`)과 동일한 폴더로 보내는 것이 좋습니다(참조).

>[!NOTE]
>
>이 설정을 변경하기 전에 새 폴더를 만들어야 합니다. Image Serving이 필요한 만들기, 읽기 및 쓰기 권한을 갖도록 액세스 권한이 설정되어 있는지 확인합니다.

## IS:TraceClient - 이미지 서버 디버그 로그 수준 {#section-3851f1f68e404430985c629ac80534db}

로그 수준은 1, 2, 3 또는 4일 수 있습니다(기본값은 2).

수준 1은 시작, 종료 및 Platform 서버 연결과 관련된 이벤트를 기록합니다.

또한 레벨 2는 소스 이미지에 연결 및 연결 끊기 기록합니다.

레벨 3은 픽셀 데이터 및 동일한 전달에 대한 요청 기록을 Platform 서버에 추가합니다.

수준 4는 Platform 서버로부터 받은 모든 메시지를 기록합니다.

로그 파일의 크기가 매우 커지기 때문에 레벨 3과 4는 디버그 목적으로만 사용해야 합니다.

## IS::TraceStatsInterval - 이미지 서버 통계 로그 간격 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

이미지 서버는 이 설정으로 지정한 간격에 따라 추적 로그 파일에 메모리 통계를 기록합니다. 유효한 범위는 5-86,400초입니다.
