---
description: 다음 단계에 따라 Windows에서 처음으로 이미지 제공을 설치합니다.
seo-description: 다음 단계에 따라 Windows에서 처음으로 이미지 제공을 설치합니다.
seo-title: 처음 설치
solution: Experience Manager
title: 처음 설치
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# 처음 설치{#installing-for-the-first-time}

다음 단계에 따라 Windows에서 처음으로 이미지 제공을 설치합니다.

1. 관리자 권한으로 서버 호스트에 로그인합니다.
1. 라이센스를 이미 받은 경우 서버에 복사한 다음 파일을 두 번 클릭하여 라이센스 설치를 실행합니다.

   아직 라이센스를 가지고 있지 않은 경우 설치를 진행하고 나중에 라이센스를 설치할 수 있습니다.
1. Image Serving 배포 zip 파일의 내용을 추출합니다.
1. [!DNL setup]/ [!DNL setup.exe]을(를) 실행하여 설치 마법사를 시작합니다.
1. &quot;다음&quot;을 클릭하여 최종 사용자 사용권 계약(EULA)으로 이동한 다음 사용권 계약을 읽고 **[!UICONTROL 예]**&#x200B;를 클릭합니다.

   다음 대화 상자가 표시됩니다.[!DNL Authentication]
1. 라이센스가 이미 설치되어 있고 라이센스 정보가 [!DNL Authentication] 대화 상자에 나타나면 **[!UICONTROL 다음]**&#x200B;을 클릭하여 계속합니다.

   라이센스가 없는 경우 **[!UICONTROL 라이선스 요청]**&#x200B;을 클릭합니다. 다음 대화 상자에는 시스템의 네트워크 인터페이스 카드 MAC 주소 중 하나가 표시됩니다. 메시지가 표시되면 이 MAC 주소, 회사 이름 및 설치 제품을 이메일로 전송합니다.

   **중요:** 라이센스는 이 호스트에 설치된 네트워크 인터페이스 카드 중 하나의 MAC 주소를 기반으로 합니다. 이 카드를 비활성화, 제거 또는 교체할 경우 라이선스는 더 이상 유효한 것으로 인식되지 않습니다. IS에 사용할 하드웨어 구성에 대한 라이센스를 받아야 합니다.

   유효한 라이센스 없이 IS를 계속 설치하고 나중에 라이센스를 설치할 수 있습니다. 계속하려면 **[!UICONTROL 뒤로]**&#x200B;를 클릭하여 [!DNL Authentication] 대화 상자로 돌아간 다음 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.
1. &quot;플랫폼 서버 관리 설정&quot; 페이지로 이동합니다. 필요에 따라 새 값을 입력하거나 기본값을 사용합니다.

   다음 항목을 구성할 수 있습니다.

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> 플랫폼 서버 HTTP 연결 포트 </p> </td> 
   <td> <p>이미지 제공 및 이미지 렌더링을 위한 기본 HTTP 수신 포트 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 관리 의견 수렴 포트 </p> </td> 
   <td> <p>관리 의견 수렴 포트 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 플랫폼 서버 캐시 크기(MB) </p> </td> 
   <td> <p>기본 응답 캐시의 초기 크기 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 플랫폼 서버 캐시 위치 </p> </td> 
   <td> <p>PS 캐시 폴더 </p> </td> 
  </tr> 
 </tbody> 
</table>

지정된 포트 번호는 고유해야 하며 다른 응용 프로그램 또는 서비스에서 사용해서는 안됩니다.

다음 화면에서는 선택한 설정을 검토할 수 있습니다.
1. **[!UICONTROL 뒤로]**&#x200B;를 클릭하여 변경하거나 **[!UICONTROL 다음]**&#x200B;을 클릭하여 설치를 시작합니다.
1. **[!UICONTROL 완료]**&#x200B;를 클릭하여 설치 마법사를 종료합니다.
