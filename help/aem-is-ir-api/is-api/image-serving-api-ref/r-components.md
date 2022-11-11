---
description: Scene 7 이미지 제공 기능은 다음 구성 요소로 구성됩니다
solution: Experience Manager
title: 이미지 제공 구성 요소
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# 이미지 제공 구성 요소{#image-serving-components}

Scene 7 Image Serving은 다음 구성 요소로 구성됩니다.

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>구성 요소 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>서버 감독자 </p> </td> 
   <td colname="col2"> <p>다른 구성 요소의 상태를 시작, 중지 및 보장할 수 있는 독립 실행형 실행 파일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>대부분의 Java 기반 구성 요소에 대한 환경을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>모니터링/경고 서비스 </p> </td> 
   <td colname="col2"> <p>J2EE 응용 프로그램. 서버 모니터링 및 전자 메일 경고를 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE 응용 프로그램. 다른 구성 요소와의 클라이언트 연결, 로깅, 통신을 관리합니다. 에서 HTTP 액세스 <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>캐싱 서비스 </p> </td> 
   <td colname="col2"> <p>J2EE 응용 프로그램. 를 관리합니다 [!DNL Platform Server]의 데이터 캐시. /is/cache에서 HTTP 액세스. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이미지 서버 </p> </td> 
   <td colname="col2"> <p>모든 이미지 처리 및 이미지 파일 I/O 작업을 수행합니다. 32비트 및 64비트 실행 파일은 모두 Linux(Windows의 경우 32비트)에서 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE 텍스트 렌더링 구성 요소 </p> </td> 
   <td colname="col2"> <p>텍스트 렌더링 서비스의 인스턴스 중 하나 이상이 <span class="codeph"> textPs=</span> 작업이 실행됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG 렌더링 구성 요소 </p> </td> 
   <td colname="col2"> <p>독립 실행형 Java 애플리케이션(Tomcat에서 호스팅되지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media 이미지 렌더링(이라고도 함). 렌더링 서버) </p> </td> 
   <td colname="col2"> <p>활성화하려면 별도의 라이센스가 필요합니다. 에서 HTTP 액세스 <span class="filepath"> /ir/render</span>. 모든 이미지 렌더링 기능은 [!DNL Platform Server] 별도의 실행 구성 요소가 없는 이미지 서버와 </p> </td> 
  </tr> 
 </tbody> 
</table>

추가 구성 설정은 기본 카탈로그( [!DNL default.ini]) 또는 특정 이미지 카탈로그( 참조) [이미지 카탈로그](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 자세한 내용).
