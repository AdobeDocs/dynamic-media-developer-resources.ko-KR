---
description: 모든 구성 파일은 install_folder/conf에 있으며 대부분의 텍스트 편집기에서 편집할 수 있습니다. 변경 사항을 적용하려면 서버를 다시 시작해야 할 수 있습니다.
solution: Experience Manager
title: 서버 구성 파일
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---

# 서버 구성 파일{#server-configuration-files}

모든 구성 파일은 install_folder/conf에 있으며 대부분의 텍스트 편집기에서 편집할 수 있습니다. 변경 사항을 적용하려면 서버를 다시 시작해야 할 수 있습니다.

>[!NOTE]
>
>대부분의 서버 구성 파일에는 이 설명서에 설명되지 않은 추가 속성과 값이 포함되어 있습니다. 이러한 속성은 내부 서버용이며 Dynamic Media 기술 지원에서 명시적으로 지시하지 않는 한 수정해서는 안 됩니다.

이 문서에서는 다음 구성 파일의 설정에 대해 설명합니다.

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>구성 파일</b> </th> 
   <th class="entry"> <b>설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>서버 감독자 구성입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat 구성 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] 구성. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>카탈로그 서비스 구성. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>서버 모니터링 구성. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>이미지 서버 구성. </p> </td> 
  </tr> 
 </tbody> 
</table>

구성 파일에 대해서는 이 문서의 후반부에 자세히 설명되어 있습니다.
