---
description: 이러한 서버 설정을 사용하여 추적 로깅을 디버깅하십시오.
solution: Experience Manager
title: Debug_trace 로깅
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Debug_trace 로깅{#debug-trace-logging}

이러한 서버 설정을 사용하여 추적 로깅을 디버깅하십시오.

>[!NOTE]
>
>모든 로그 파일이 와 동일한 폴더에 작성되도록 구성하는 것이 좋습니다 `TC::directory`. 이렇게 하면 모든 이미지 제공 로그 파일이 `TC::maxDays`: 디스크 공간 부족 조건으로 인해 서버 불안정을 방지할 수 있습니다.

## SV::log - 서버 감독자 추적 로그 파일 경로 {#section-3697bc480ff646e79cacc2812c55ef26}

서버 감독자 로그 파일의 폴더 및 기본 파일 이름입니다. 경로는 절대 또는 상대적일 수 있습니다 *[!DNL install_folder]*. 서버 감독자가 하이픈과 현재 날짜( *[!DNL -yyyy-mm-dd]*)를 파일 이름에 추가합니다(파일 접미사 앞에 있는 경우). 모든 로그 파일을 [!DNL Platform Server] 로그 파일 ( `PS::LogFolder`)을 사용하여 [!DNL Platform Server] ( `PS::LogDays`). 기본값은 입니다. [!DNL logs/Supervisor.log].

>[!NOTE]
>
>이 설정을 변경하기 전에 새 폴더를 만들어야 합니다. 서버 관리자가 필요한 생성, 읽기 및 쓰기 권한을 갖도록 액세스 권한이 설정되어 있는지 확인합니다.

## SV::tracelevel - 서버 감독자 추적 로그 수준 {#section-36f8634741da4c618d67aa628b5fe474}

로그 수준은 1, 2, 3 또는 4일 수 있습니다. 기본값은 2입니다.

## IS::Log - 이미지 서버 디버그 로그 파일 경로 {#section-73a3f09b77f2446c9f82207b7d8aec39}

이미지 서버 추적 로그 파일의 폴더 및 기본 파일 이름입니다. 경로는 절대 또는 상대적일 수 있습니다 *[!DNL install_folder]*. ImageServer에 하이픈과 현재 날짜( *[!DNL -yyyy-mm-dd]*)를 파일 이름에 추가합니다(파일 접미사 앞에 있는 경우). 이미지 서버 로그 파일을 와 동일한 폴더로 보내는 것이 좋습니다 [!DNL Platform Server] 로그 파일 ( `PS::LogFolder`)을 사용하여 [!DNL Platform Server] 자세한 내용은 `PS::LogDays`).

>[!NOTE]
>
>이 설정을 변경하기 전에 새 폴더를 만들어야 합니다. 이미지 제공 시 필요한 작성, 읽기 및 쓰기 권한이 부여되도록 액세스 권한이 설정되었는지 확인합니다.

## IS:TraceClient - 이미지 서버 디버그 로그 수준 {#section-3851f1f68e404430985c629ac80534db}

로그 수준은 1, 2, 3 또는 4일 수 있습니다(기본값은 2).

수준 1은 시작, 종료 및 와 관련된 이벤트를 기록합니다 [!DNL Platform Server] 연결.

또한 레벨 2는 소스 이미지에 연결 및 연결을 끊습니다.

레벨 3은 픽셀 데이터 및 전송에 대한 요청 로깅을 [!DNL Platform Server].

레벨 4 는 [!DNL Platform Server].

로그 파일이 매우 커질 수 있으므로 레벨 3 및 4는 디버그 목적으로만 사용해야 합니다.

## IS::TraceStatsInterval - 이미지 서버 통계 로그 간격 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

이미지 서버는 이 설정에 지정된 간격에 따라 추적 로그 파일에 메모리 통계를 기록합니다. 유효한 범위는 5-86,400초입니다.
