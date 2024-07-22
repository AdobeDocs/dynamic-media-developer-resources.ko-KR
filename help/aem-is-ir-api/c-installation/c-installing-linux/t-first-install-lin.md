---
title: 처음 설치
description: 이 절차에서는 Linux®에서 처음으로 이미지 서비스를 설치하는 방법을 보여 줍니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# 처음 설치{#installing-for-the-first-time}

이 절차에서는 Linux®에서 처음으로 이미지 서비스를 설치하는 방법을 보여 줍니다.

1. 루트 권한으로 서버 호스트에 로그인합니다.
1. [!DNL /usr/local/scene7/licenses] 폴더를 만듭니다.

   이미지 제공 및/또는 이미지 렌더링 라이선스 키 파일([!DNL .sc8] 파일 접미사 포함)을 사용할 수 있는 경우 이 폴더에 복사하십시오. 그렇지 않으면 설치를 계속하고 나중에 라이센스 키를 설치하십시오.
1. 이미지 제공 배포 tar 파일의 압축을 풀고 타르를 풉니다.
1. [!DNL Setup] 폴더에서 [!DNL ./install-is]을(를) 실행하여 설치 마법사를 시작합니다.

   라이센스 키가 없으면 라이센스 파일을 가져오는 방법을 설명하는 지침이 표시됩니다. 이 시점에서 설치하거나 이미지 서버 설치를 계속 진행하고 나중에 라이센스 키를 설치하십시오.
1. EULA(최종 사용자 사용권 계약)가 표시되면 사용권 계약을 읽은 다음 계속하려면 `y`을(를) 입력하십시오.

   다음 표에 나열된 프롬프트가 표시됩니다.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 주 수신 대기 포트 [8080]:</span> </p> </td>
   <td colname="col2"> <p>이미지 제공 및 이미지 렌더링용 기본 HTTP 수신 포트입니다. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 관리자 수신 대기 포트 [8083]:</span> </p> </td> 
   <td colname="col2"> <p>관리자 수신 포트입니다. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 최대 HTTP 캐시 크기(MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>기본 응답 캐시의 초기 크기입니다. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 캐시 루트 폴더 [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS 캐시 폴더 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 이미지 서버 소유자 ID [루트]:</span> </p> </td>
   <td colname="col2"> <p>이미지 제공 서버를 설치할 사용자 계정입니다. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 이미지 서버 그룹 ID [루트]:</span> </p> </td>
   <td colname="col2"> <p>이미지 제공 서버를 설치할 그룹 계정입니다. </p> </td>
  </tr>
 </tbody>
</table>

1. 기본값을 사용하거나 다른 값을 지정하려면 **[!UICONTROL Enter]**&#x200B;를 누르십시오.

   지정된 모든 포트 번호가 고유하고 이 호스트에서 다른 방법으로 사용되지 않는지 확인하십시오.

   >[!IMPORTANT]
   >
   >루트 이외의 계정을 지정한 경우 구성 파일에서 이러한 폴더를 재구성할 때 이미지 서버에서 읽고 쓰는 데 필요한 모든 파일 및 폴더에 대한 액세스 권한이 올바르게 설정되었는지 확인해야 합니다.
   >
   >이제 [!DNL /usr/local/Scene7/ImageServing]에 이미지 제공이 설치되었습니다. 특정 이미지 렌더링 콘텐츠가 [!DNL /usr/local/Scene7/ImageRendering]에 설치되어 있습니다.
   >
   >설치가 끝날 때 설치 마법사는 이미지 서버 시작을 시도합니다. 유효한 라이선스 키가 없으면 이미지 서버를 시작할 수 없습니다. 유효한 라이센스가 있고 이미지 서버가 여전히 시작되지 않는 경우 로그 파일을 참조하십시오.

>[!NOTE]
>
>이미지 서비스 제공 설치 후 라이센스가 설치된 경우 사용하기 전에 이미지 서버를 수동으로 시작해야 합니다.
