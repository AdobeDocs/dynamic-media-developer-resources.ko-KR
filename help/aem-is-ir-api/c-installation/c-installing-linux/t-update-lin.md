---
description: Linux에서 Scene7 이미지 제공을 업그레이드할 때 이 절차를 사용합니다.
seo-description: Linux에서 Scene7 이미지 제공을 업그레이드할 때 이 절차를 사용합니다.
seo-title: IS 4.7.4 이상에서 업데이트
solution: Experience Manager
title: IS 4.7.4 이상에서 업데이트
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IS 4.7.4 이상에서 업데이트{#updating-from-is-or-later}

Linux에서 Scene7 이미지 제공을 업그레이드할 때 이 절차를 사용합니다.

이전 버전의 이미지 제공에서 업그레이드하는 경우 올바른 프로세스에 대해서는 지원 센터에 문의하십시오.

업그레이드 시 [!DNL webapps] 폴더가 삭제될 수 있습니다. 업그레이드하기 전에 [!DNL webapps] 폴더를 백업하십시오.

1. 루트 권한으로 서버 호스트에 로그인합니다.
1. 이미지 제공 배포 tar 파일의 압축을 풀고 압축을 해제합니다.
1. 을 [!DNL ./install-is] 실행하여 [!DNL setup] 폴더에 있는 설치 마법사를 시작합니다.

   업데이트 설치 관리자는 설치된 패키지의 무결성 및 버전을 확인합니다. 성공하면 최종 사용자 사용권 계약(&quot;EULA&quot;)이 표시됩니다.
1. 라이센스 계약을 읽은 다음 &quot; **[!UICONTROL y]**&quot;를 입력하여 설치를 계속합니다.

   설치 관리자가 이전 서버 구성 파일을 [!DNL BACKUP/] 폴더에 백업합니다.

   설치가 완료되면 다음 메시지가 표시됩니다.

   `Image Server was started successfully`
>업데이트 중에 파일이 최신 설정으로 [!DNL ImageServing/conf/server.xml] 업데이트됩니다. 값을 변경하거나 추가한 경우 기존 값을 저장하고 업그레이드 후 변경 내용을 [!DNL server.xml] 다시 구현해야 합니다.
>
>업데이트 설치 후 서버를 라이브하기 전에 HTTP 응답 캐시를 다시 구성하는 것이 좋습니다. 자세한 내용은 유틸리티의 [!DNL playlog] 설명을 참조하십시오.

