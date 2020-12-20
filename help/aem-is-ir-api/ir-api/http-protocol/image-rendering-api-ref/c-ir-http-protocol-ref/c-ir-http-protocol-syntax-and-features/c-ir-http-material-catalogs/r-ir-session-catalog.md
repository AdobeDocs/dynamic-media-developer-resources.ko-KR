---
description: 세션 카탈로그는 모든 src=, vignette= 및 icc= 명령에 대한 기본 catId 값과 요청에 대한 세션 특성을 제공하는 자료 카탈로그입니다.
seo-description: 세션 카탈로그는 모든 src=, vignette= 및 icc= 명령에 대한 기본 catId 값과 요청에 대한 세션 특성을 제공하는 자료 카탈로그입니다.
seo-title: 세션 카탈로그
solution: Experience Manager
title: 세션 카탈로그
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# 세션 카탈로그{#session-catalog}

세션 카탈로그는 모든 src=, vignette= 및 icc= 명령에 대한 기본 catId 값과 요청에 대한 세션 특성을 제공하는 자료 카탈로그입니다.

세션 카탈로그는 서버 이름 바로 다음에 있는 HTTP 요청 경로의 첫 번째 경로 요소로 지정됩니다. 첫 번째 경로 요소가 카탈로그의 특성::RootId와 일치하지 않으면 기본 카탈로그가 세션 카탈로그로 사용됩니다.

세션 카탈로그는 다음과 같은 세션 기본값을 제공합니다.

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>속성 </p> </th> 
   <th class="entry"> <p>주의 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::RootPath</span> </p> </td> 
   <td> <p> 재료 데이터 파일의 루트 경로 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::VignettePath</span> </p> </td> 
   <td> <p> 비네팅 파일의 루트 경로 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::IccProfileRgb</span> </p> </td> 
   <td> <p> 비네팅에 ICC 프로파일이 포함되지 않는 경우 기본 작업 색상 공간 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::RootUrl</span> </p> </td> 
   <td> <p> <span class="codeph"> src=</span> 명령의 상대 HTTP 파일 경로에 대한 루트 URL </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::ShowOverlapObjects</span> </p> </td> 
   <td> <p> 겹쳐진 개체의 초기 표시/숨기기 상태 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::만료</span> </p> </td> 
   <td> <p> 프록시 서버 및 브라우저 캐시에 대한 응답 이미지의 실시간 값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::MaxPix</span> </p> </td> 
   <td> <p> 허용되는 최대 응답 이미지 폭 및 높이 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::DefaultPix</span> </p> </td> 
   <td> <p> <span class="codeph"> with=</span> 및 <span class="codeph"> hei=</span>의 기본값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::Format</span> </p> </td> 
   <td> <p> <span class="codeph"> fmt=</span>의 기본값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::JpegQuality</span> </p> </td> 
   <td> <p> <span class="codeph"> qlt=</span>의 기본값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::TiffEncoding</span> </p> </td> 
   <td> <p> TIFF 이미지 출력에 대한 압축 유형 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::선명 효과</span> </p> </td> 
   <td> <p> <span class="codeph"> 선명하게=</span>의 기본값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::OnFailSel</span> </p> </td> 
   <td> <p> <span class="codeph"> sel=</span> 명령이 실패할 때 동작을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> <span class="codeph"> obj=</span> 명령이 실패할 때 동작을 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

