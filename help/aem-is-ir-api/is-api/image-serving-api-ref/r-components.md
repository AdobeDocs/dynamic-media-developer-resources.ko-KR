---
description: 'Scene 7 이미지 제공 구성 요소는 다음과 같습니다. '
seo-description: 'Scene 7 이미지 제공 구성 요소는 다음과 같습니다. '
seo-title: 이미지 제공 구성 요소
solution: Experience Manager
title: 이미지 제공 구성 요소
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 84e04972-32ce-4aca-aae6-d5b8bbe761e6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 2%

---


# 이미지 제공 구성 요소{#image-serving-components}

Scene 7 이미지 제공은 다음 구성 요소로 구성됩니다.

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>구성 요소 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>서버 관리자 </p> </td> 
   <td colname="col2"> <p>다른 구성 요소의 상태를 시작, 중지 및 유지하는 작업을 담당하는 독립형 실행 파일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>대부분의 Java 기반 구성 요소에 대한 환경을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>모니터링/경고 서비스 </p> </td> 
   <td colname="col2"> <p>J2EE 응용 프로그램. 서버 모니터링 및 이메일 경고를 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>플랫폼 서버 </p> </td> 
   <td colname="col2"> <p>J2EE 응용 프로그램. 클라이언트 연결, 로깅, 다른 구성 요소와 통신을 관리합니다. <span class="filepath"> /is/image</span>에서 HTTP 액세스 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>캐싱 서비스 </p> </td> 
   <td colname="col2"> <p>J2EE 응용 프로그램. 플랫폼 서버의 데이터 캐시를 관리합니다. /is/cache에서 HTTP 액세스. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이미지 서버 </p> </td> 
   <td colname="col2"> <p>모든 이미지 처리 및 이미지 파일 I/O 작업을 수행합니다. 32비트 및 64비트 실행 파일은 모두 Linux에서 사용할 수 있습니다(Windows의 경우 32비트만 해당). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>텍스트 렌더링 구성 요소 날짜 </p> </td> 
   <td colname="col2"> <p><span class="codeph"> textPs=</span> 작업이 실행되면 하나 이상의 텍스트 렌더링 서비스 인스턴스가 활성 상태일 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG 렌더링 구성 요소 </p> </td> 
   <td colname="col2"> <p>독립 실행형 Java 응용 프로그램(Tomcat에서 호스팅되지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media 이미지 렌더링(일명. 렌더링 서버) </p> </td> 
   <td colname="col2"> <p>활성화하려면 별도의 라이선스가 필요합니다. <span class="filepath"> /ir/render</span>에서 HTTP 액세스. 모든 이미지 렌더링 기능은 별도의 실행 구성 요소가 없이 플랫폼 서버 및 이미지 서버에 통합됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

추가 구성 설정은 기본 카탈로그( [!DNL default.ini]) 또는 특정 이미지 카탈로그(자세한 내용은 [이미지 카탈로그](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 참조)에서 제공됩니다.
