---
title: IS 4.7.4 이상에서 업데이트
description: Dynamic Media 이미지 서비스 제공 업그레이드 시 이 절차를 사용하십시오.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# IS 4.7.4 이상에서 업데이트{#updating-from-is-or-later}

Dynamic Media 이미지 서비스 제공 업그레이드 시 이 절차를 사용하십시오.

이전 버전의 이미지 제공에서 업그레이드하는 경우, 올바른 프로세스에 대해 지원 센터에 문의하십시오.

>[!NOTE]
>
>다음 [!DNL webapps] 업그레이드 시 폴더가 삭제될 수 있습니다. 백업 [!DNL webapps] 업그레이드 전 폴더

1. 관리 권한을 사용하여 서버 호스트에 로그인합니다.
1. 이미지 제공 배포 zip 파일의 컨텐츠를 추출합니다.
1. 를 실행하여 설치 마법사를 시작합니다. `setup/setup.exe`.
1. 선택 **[!UICONTROL 다음]** 최종 사용자 사용권 계약(EULA)으로 이동하려면 사용권 계약을 읽고 다음을 선택합니다 **[!UICONTROL 예]**.

   다음 페이지에는 이전 구성 설정이 표시됩니다.
1. 클릭 **[!UICONTROL 다음]** 업데이트 설치를 시작합니다.

   >[!NOTE]
   >
   >설치 관리자는 이전 서버 구성 파일을 [!DNL BACKUP/] 폴더를 삭제합니다.

1. 설치가 완료되면 다음을 선택합니다. **[!UICONTROL 완료]** 설치 마법사를 종료합니다.

   경우에 따라 설치 마법사에서 시스템을 재부팅하도록 요청할 수 있습니다.

업데이트 중에 [!DNL ImageServing/conf/server.xml] 파일이 최신 설정으로 업데이트되었습니다. 값을 변경하거나 추가한 경우 기존 값을 저장해야 합니다 [!DNL server.xml] 업그레이드 후 변경 사항을 다시 구현합니다.

업데이트 설치 후 서버를 라이브로 전환하기 전에 HTTP 응답 캐시를 워밍업하는 것이 좋습니다. 다음에 대한 설명을 참조하십시오. `playlog` 유틸리티입니다.
