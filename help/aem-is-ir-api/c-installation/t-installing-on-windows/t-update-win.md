---
description: Dynamic Media Image Serving을 업그레이드할 때 이 절차를 사용하십시오.
seo-description: Dynamic Media Image Serving을 업그레이드할 때 이 절차를 사용하십시오.
seo-title: IS 4.7.4 이상에서 업데이트
solution: Experience Manager
title: IS 4.7.4 이상에서 업데이트
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# IS 4.7.4 이상{#updating-from-is-or-later}에서 업데이트

Dynamic Media Image Serving을 업그레이드할 때 이 절차를 사용하십시오.

이전 버전의 Image Serving에서 업그레이드하는 경우 올바른 프로세스에 대해서는 지원 센터에 문의하십시오.

>[!NOTE]
>
>업그레이드 시 [!DNL webapps] 폴더를 삭제할 수 있습니다. 업그레이드하기 전에 [!DNL webapps] 폴더를 백업합니다.

1. 관리자 권한으로 서버 호스트에 로그인합니다.
1. Image Serving 배포 zip 파일의 내용을 추출합니다.
1. setup/setup.exe을 실행하여 설치 마법사를 시작합니다.
1. **[!UICONTROL 다음]**&#x200B;을 클릭하여 EULA(최종 사용자 사용권 계약)로 이동한 다음 사용권 계약을 읽은 후 **[!UICONTROL 예]**&#x200B;를 클릭합니다.

   다음 페이지에는 이전 구성 설정이 표시됩니다.
1. 업데이트 설치를 시작하려면 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >설치 관리자가 이전 서버 구성 파일을 [!DNL BACKUP/] 폴더에 백업합니다.

1. 설치가 완료되면 &quot;마침&quot;을 클릭하여 설치 마법사를 종료합니다.

   경우에 따라 설치 마법사가 시스템을 재부팅하도록 요청할 수 있습니다.

업데이트하는 동안 [!DNL ImageServing/conf/server.xml] 파일이 최신 설정으로 업데이트됩니다. 값을 변경하거나 추가한 경우 기존 [!DNL server.xml]을(를) 저장하고 업그레이드 후 변경 내용을 다시 구현해야 합니다.

업데이트 설치 후 서버를 라이브하기 전에 HTTP 응답 캐시를 따뜻하게 하는 것이 좋습니다. 자세한 내용은 `playlog` 유틸리티의 설명을 참조하십시오.
