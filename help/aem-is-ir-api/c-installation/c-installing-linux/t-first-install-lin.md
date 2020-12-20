---
description: 이 절차에서는 Linux에서 처음으로 이미지 제공을 설치하는 방법을 보여 줍니다.
seo-description: 이 절차에서는 Linux에서 처음으로 이미지 제공을 설치하는 방법을 보여 줍니다.
seo-title: 처음 설치
solution: Experience Manager
title: 처음 설치
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# 처음 설치{#installing-for-the-first-time}

이 절차에서는 Linux에서 처음으로 이미지 제공을 설치하는 방법을 보여 줍니다.

1. 루트 권한으로 서버 호스트에 로그인합니다.
1. [!DNL /usr/local/scene7/licenses] 폴더를 만듭니다.

   이미지 제공 및/또는 이미지 렌더링 라이선스 키 파일([!DNL .sc8] 파일 접미사 포함)을 사용할 수 있으면 이 폴더에 복사합니다. 그렇지 않은 경우 설치를 진행하고 나중에 라이센스 키를 설치합니다.
1. 이미지 제공 배포 tar 파일의 압축을 풀고 압축을 해제합니다.
1. [!DNL Setup] 폴더에 있는 [!DNL ./install-is]을 실행하여 설치 마법사를 시작합니다.

   라이센스 키를 찾을 수 없으면 라이센스 파일을 얻는 방법을 설명하는 지침이 표시됩니다. 이 시점에서 이렇게 하거나 이미지 제공 설치를 계속 진행하고 나중에 라이센스 키를 설치합니다.
1. 최종 사용자 사용권 계약(EULA)이 표시되면 사용권 계약을 읽은 다음 `y`을 입력하여 계속 진행합니다.

   다음 표에 나열된 메시지가 설치 관리자에 표시됩니다.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 기본 의견 수렴 포트 [8080]:</span> </p> </td> 
   <td colname="col2"> <p>이미지 제공 및 이미지 렌더링을 위한 기본 HTTP 수신 포트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 관리 의견 수렴 포트 [8083]:</span> </p> </td> 
   <td colname="col2"> <p>관리 수신 대기 포트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 최대 HTTP 캐시 크기(MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>기본 응답 캐시의 초기 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 캐시 루트 폴더 [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS 캐시 폴더. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 이미지 서버 소유자 ID [루트]:</span> </p> </td> 
   <td colname="col2"> <p>Image Serving 서버를 설치할 사용자 계정. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 이미지 서버 그룹 ID [루트]:</span> </p> </td> 
   <td colname="col2"> <p>이미지 제공 서버를 설치할 그룹 계정. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. **[!UICONTROL Enter]**&#x200B;를 눌러 기본값을 적용하거나 다른 값을 지정합니다.

   지정된 모든 포트 번호가 고유하며 이 호스트에서 다른 방법으로 사용되지 않아야 합니다.

   >[!IMPORTANT]
   >
   >루트 이외의 계정을 지정한 경우, 이미지 서버에서 읽고/또는 쓰기에 필요한 모든 파일 및 폴더에 대한 액세스 권한이 구성 파일에서 이러한 폴더를 다시 구성할 때 올바르게 설정되도록 해야 합니다.
   >
   >이제 이미지 제공 기능이 [!DNL /usr/local/Scene7/ImageServing]에 설치됩니다. 특정 이미지 렌더링 내용이 [!DNL /usr/local/Scene7/ImageRendering]에 설치됩니다.
   >
   >설치가 끝날 때 설치 마법사가 이미지 서버를 시작합니다. 유효한 라이센스 키를 찾을 수 없으면 이미지 서버를 시작할 수 없습니다. 유효한 라이센스가 있고 이미지 서버가 아직 시작되지 않는 경우에는 로그 파일을 참조하십시오.

>[!NOTE]
>
>Image Serving을 설치한 후 라이센스가 설치된 경우 사용하기 전에 이미지 서버를 수동으로 시작해야 합니다.
