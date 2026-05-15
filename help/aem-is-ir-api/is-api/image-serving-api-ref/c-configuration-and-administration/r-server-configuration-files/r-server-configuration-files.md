---
title: 서버 구성 파일
description: 모든 구성 파일은 install_folder/conf에 있으며 대부분의 텍스트 편집기에서 편집할 수 있습니다. 변경 사항을 적용하려면 서버를 다시 시작하십시오.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
TQID: 'https://experienceleague.adobe.com/Gp1W--QzWptazkc1ygnmw59lO8zrNmgmabYMOz8jUG4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 0%

---

# 서버 구성 파일{#server-configuration-files}

모든 구성 파일은 `install_folder/conf`에 있으며 대부분의 텍스트 편집기에서 편집할 수 있습니다. 변경 사항을 적용하려면 서버를 다시 시작하십시오.

>[!NOTE]
>
>대부분의 서버 구성 파일에는 이 설명서에 설명되지 않은 추가 속성과 값이 포함되어 있습니다. 이러한 속성은 내부 서버용이며 Dynamic Media 기술 지원에서 지시하지 않는 한 수정해서는 안 됩니다.

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
