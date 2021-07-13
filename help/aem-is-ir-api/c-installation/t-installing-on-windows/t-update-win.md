---
description: Dynamic Media Image Serving을 업그레이드할 때 이 절차를 사용하십시오.
solution: Experience Manager
title: IS 4.7.4 이상에서 업데이트
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# IS 4.7.4 이상에서 업데이트{#updating-from-is-or-later}

Dynamic Media Image Serving을 업그레이드할 때 이 절차를 사용하십시오.

이전 버전의 Image Serving에서 업그레이드하는 경우 올바른 프로세스에 대해서는 지원 팀에 문의하십시오.

>[!NOTE]
>
>업그레이드 시 [!DNL webapps] 폴더를 삭제할 수 있습니다. 업그레이드하기 전에 [!DNL webapps] 폴더를 백업합니다.

1. 관리 권한으로 서버 호스트에 로그인합니다.
1. 이미지 제공 배포 zip 파일의 컨텐츠를 추출합니다.
1. setup/setup.exe 를 실행하여 설치 마법사를 시작합니다.
1. **[!UICONTROL 다음]**&#x200B;을 클릭하여 EULA(최종 사용자 사용권 계약)로 이동한 후 사용권 계약을 읽고 **[!UICONTROL 예]**&#x200B;를 클릭합니다.

   다음 페이지에는 이전 구성 설정이 표시됩니다.
1. **[!UICONTROL 다음]**&#x200B;을 클릭하여 업데이트 설치를 시작합니다.

   >[!NOTE]
   >
   >설치 관리자가 이전 서버 구성 파일을 [!DNL BACKUP/] 폴더에 백업합니다.

1. 설치가 완료되면 &quot;마침&quot;을 클릭하여 설치 마법사를 종료합니다.

   경우에 따라 설치 마법사가 시스템을 재부팅하도록 요청할 수 있습니다.

업데이트 중에 [!DNL ImageServing/conf/server.xml] 파일이 최신 설정으로 업데이트됩니다. 값을 변경하거나 추가한 경우 기존 [!DNL server.xml]을 저장하고 업그레이드 후 변경 사항을 다시 구현해야 합니다.

업데이트 설치 후 서버를 라이브로 전환하기 전에 HTTP 응답 캐시를 따뜻하게 하는 것이 좋습니다. 자세한 내용은 `playlog` 유틸리티의 설명을 참조하십시오.
