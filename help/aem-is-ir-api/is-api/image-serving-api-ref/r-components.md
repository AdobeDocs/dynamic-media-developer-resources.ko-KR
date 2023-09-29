---
title: 이미지 제공 구성 요소
description: Dynamic Media 이미지 제공은 다음 구성 요소로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# 이미지 제공 구성 요소{#image-serving-components}

Dynamic Media 이미지 제공은 다음 구성 요소로 구성됩니다.

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
   <td colname="col2"> <p>다른 구성 요소의 시작, 중지 및 상태 보장을 담당하는 독립 실행형 실행 파일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>대부분의 Java 기반 구성 요소에 환경을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>모니터링/경고 서비스 </p> </td> 
   <td colname="col2"> <p>J2EE 애플리케이션. 서버 모니터링 및 이메일 경고 기능을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE 애플리케이션. 클라이언트 연결, 로깅, 다른 구성 요소와의 통신을 관리합니다. 다음 위치의 HTTP 액세스 <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>캐싱 서비스 </p> </td> 
   <td colname="col2"> <p>J2EE 애플리케이션. 관리 [!DNL Platform Server]의 데이터가 캐시됩니다. /is/cache에서 HTTP 액세스. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이미지 서버 </p> </td> 
   <td colname="col2"> <p>모든 이미지 처리 및 이미지 파일 I/O 작업을 수행합니다. 32비트 및 64비트 실행 파일은 모두 Linux®에서 사용할 수 있습니다(32비트는 Windows에서만 사용). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>텍스트 렌더링 구성 요소 생성 </p> </td> 
   <td colname="col2"> <p>텍스트 렌더링 서비스의 하나 이상의 인스턴스는 다음의 경우에 활성화될 수 있다 <span class="codeph"> textPs=</span> 작업이 실행됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG 렌더링 구성 요소 </p> </td> 
   <td colname="col2"> <p>독립형 Java™ 애플리케이션(Tomcat에서 호스팅하지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media 이미지 렌더링(예: 렌더링 서버) </p> </td> 
   <td colname="col2"> <p>활성화하려면 별도의 라이센스가 필요합니다. 다음 위치의 HTTP 액세스 <span class="filepath"> /ir/render</span>. 모든 이미지 렌더링 기능이 [!DNL Platform Server] 별도의 실행 가능한 구성 요소가 없는 이미지 서버입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

추가 구성 설정은 기본 카탈로그( [!DNL default.ini]) 또는 특정 이미지 카탈로그(참조 [이미지 카탈로그](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 을 참조하십시오.
