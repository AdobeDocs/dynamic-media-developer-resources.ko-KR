---
title: 처음 설치
description: 이 단계를 사용하여 Windows에서 처음으로 이미지 제공 서비스를 설치합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# 처음 설치{#installing-for-the-first-time}

이 단계를 사용하여 Windows에서 처음으로 이미지 제공 서비스를 설치합니다.

1. 관리 권한으로 서버 호스트에 로그인합니다.
1. 라이센스를 이미 받은 경우 서버에 복사한 다음 파일을 두 번 클릭하여 라이센스 설치를 실행합니다.

   아직 라이센스가 없는 경우 설치를 진행하고 나중에 라이센스를 설치할 수 있습니다.

1. 이미지 제공 배포 zip 파일의 컨텐츠를 추출합니다.
1. 실행 중인 설치 마법사를 시작합니다. [!DNL setup]/ [!DNL setup.exe].
1. 선택 **[!UICONTROL 다음]** 최종 사용자 사용권 계약(EULA)으로 이동하려면 사용권 계약을 읽고 **[!UICONTROL 예]**.

   다음 [!DNL Authentication] 다음 대화 상자가 표시됩니다.
1. 라이센스가 이미 설치되어 있고 라이센스 정보가 [!DNL Authentication] 대화 상자, 선택 **[!UICONTROL 다음]** 계속하십시오.

   라이센스가 없는 경우 **[!UICONTROL 라이선스 요청]**. 다음 대화 상자에는 시스템의 네트워크 인터페이스 카드 MAC 주소 중 하나가 표시됩니다. 프롬프트에 따라 이 MAC 주소, 회사 이름 및 설치 제품을 이메일로 보냅니다.

   **중요 사항:** 라이센스는 이 호스트에 설치된 네트워크 인터페이스 카드 중 하나의 MAC 주소를 기반으로 합니다. 이 카드를 사용 안 함, 제거 또는 교체하면 라이센스가 더 이상 유효한 것으로 인식되지 않습니다. 이미지 제공 시 사용하는 하드웨어 구성에 대한 라이센스를 받아야 합니다.

   유효한 라이센스 없이 IS 를 계속 설치하고 나중에 라이센스를 설치할 수 있습니다. 계속하려면 을(를) 선택합니다. **[!UICONTROL 뒤로]** 로 돌아가기 [!DNL Authentication] 대화 상자를 선택한 다음 **[!UICONTROL 다음]**.
1. &quot;Platform Server 관리 설정&quot; 페이지로 이동합니다. 필요에 따라 새 값을 입력하거나 기본값을 적용합니다.

   다음 항목을 구성할 수 있습니다.

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> Platform Server HTTP 연결 포트 </p> </td>
      <td> <p>이미지 제공 및 이미지 렌더링을 위한 기본 HTTP 수신 포트 </p> </td>
   </tr> 
   <tr> 
      <td> <p> 관리 수신 대기 포트 </p> </td>
      <td> <p>관리 수신 대기 포트 </p> </td>
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

   지정한 포트 번호는 고유해야 하며 다른 응용 프로그램 또는 서비스에서 사용하지 않아야 합니다.

   다음 화면에서는 선택한 설정을 검토할 수 있습니다.

1. 선택 **[!UICONTROL 뒤로]** 변경하려면 다음을 선택하고 **[!UICONTROL 다음]** 를 클릭하여 설치를 시작합니다.

1. 선택 **[!UICONTROL 완료]** 를 클릭하여 설치 마법사를 종료합니다.
