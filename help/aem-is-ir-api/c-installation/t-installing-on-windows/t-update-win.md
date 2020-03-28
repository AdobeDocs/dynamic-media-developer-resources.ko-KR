---
description: Scene7 이미지 제공을 업그레이드할 때 이 절차를 사용합니다.
seo-description: Scene7 이미지 제공을 업그레이드할 때 이 절차를 사용합니다.
seo-title: IS 4.7.4 이상에서 업데이트
solution: Experience Manager
title: IS 4.7.4 이상에서 업데이트
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IS 4.7.4 이상에서 업데이트{#updating-from-is-or-later}

Scene7 이미지 제공을 업그레이드할 때 이 절차를 사용합니다.

이전 버전의 이미지 제공에서 업그레이드하는 경우 올바른 프로세스에 대해서는 지원 센터에 문의하십시오.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>업그레이드 시 [!DNL webapps] 폴더가 삭제될 수 있습니다. 업그레이드하기 전에 [!DNL webapps] 폴더를 백업합니다.

1. 관리 권한으로 서버 호스트에 로그인합니다.
1. 이미지 제공 배포 zip 파일의 컨텐츠를 추출합니다.
1. setup/setup.exe을 실행하여 설치 마법사를 시작합니다.
1. [ **[!UICONTROL 다음]** ]을 클릭하여 EULA(End User License Agreement)로 이동한 다음 사용권 계약을 읽은 후 [예]를 **[!UICONTROL 클릭합니다]**.

   다음 페이지에는 이전 구성 설정이 표시됩니다.
1. 다음을 **[!UICONTROL 클릭하여]** 업데이트 설치를 시작합니다.

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >설치 관리자가 이전 서버 구성 파일을 [!DNL BACKUP/] 폴더에 백업합니다.

1. 설치가 완료되면 &quot;마침&quot;을 클릭하여 설치 마법사를 종료합니다.

   경우에 따라 설치 마법사가 시스템을 재부팅하도록 요청할 수 있습니다.
>업데이트 중에 파일이 최신 설정으로 [!DNL ImageServing/conf/server.xml] 업데이트됩니다. 값을 변경하거나 추가한 경우 기존 값을 저장하고 업그레이드 후 변경 내용을 [!DNL server.xml] 다시 구현해야 합니다.
>
>업데이트 설치 후 서버를 라이브하기 전에 HTTP 응답 캐시를 다시 구성하는 것이 좋습니다. 자세한 내용은 유틸리티의 `playlog` 설명을 참조하십시오.

