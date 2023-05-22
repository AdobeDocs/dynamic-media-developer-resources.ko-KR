---
title: IS 4.7.4 이상에서 업데이트
description: Linux®에서 Dynamic Media 이미지 제공 기능을 업그레이드할 때 이 절차를 따르십시오.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# IS 4.7.4 이상에서 업데이트{#updating-from-is-or-later}

Linux®에서 Dynamic Media 이미지 제공 기능을 업그레이드할 때 이 절차를 따르십시오.

이전 버전의 이미지 제공에서 업그레이드하는 경우, 올바른 프로세스에 대해 지원 센터에 문의하십시오.

다음 [!DNL webapps] 업그레이드 시 폴더를 삭제할 수 있습니다. 다음을 백업하십시오. [!DNL webapps] 업그레이드 전 폴더

1. 루트 권한으로 서버 호스트에 로그인합니다.
1. 이미지 제공 배포 tar 파일의 압축을 풀고 타르를 풉니다.
1. 다음에서 [!DNL setup] 폴더, 실행 [!DNL `./install-is`] 설치 마법사를 시작합니다.

   업데이트 설치 관리자가 설치된 패키지의 무결성과 버전을 확인합니다. 성공하면 최종 사용자 사용권 계약(&quot;EULA&quot;)이 표시됩니다.
1. 사용권 계약을 읽고 다음을 입력하십시오. **[!UICONTROL y]** 을 클릭하여 설치를 계속합니다.

   설치 관리자는 이전 서버 구성 파일을 [!DNL BACKUP/] 폴더를 삭제합니다.

   설치가 완료되면 다음과 같은 메시지가 표시됩니다.

   `Image Server was started successfully`

업데이트 중에 [!DNL ImageServing/conf/server.xml] 파일이 최신 설정으로 업데이트되었습니다. 값을 변경하거나 추가한 경우 기존 값을 저장합니다 [!DNL server.xml] 업그레이드 후 변경 사항을 다시 구현합니다.

업데이트 설치 후 서버를 라이브로 전환하기 전에 HTTP 응답 캐시를 워밍업하는 것이 좋습니다. 다음에 대한 설명을 참조하십시오. [!DNL playlog] 유틸리티입니다.
