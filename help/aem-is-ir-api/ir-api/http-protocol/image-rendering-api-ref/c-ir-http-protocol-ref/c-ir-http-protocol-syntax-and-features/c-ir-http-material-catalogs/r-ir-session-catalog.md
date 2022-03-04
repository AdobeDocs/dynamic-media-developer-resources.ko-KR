---
title: 세션 카탈로그
description: 세션 카탈로그는 요청에 대한 세션 속성을 제공하는 자료 카탈로그이며 모든 src=, vignette= 및 icc= 명령에 대한 기본 catId 값입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 세션 카탈로그{#session-catalog}

세션 카탈로그는 요청에 대한 세션 속성을 제공하는 자료 카탈로그이며 모든 항목에 대한 기본 catId 값입니다 `src=`, `vignette=`, 및 `icc=` 명령.

세션 카탈로그는 HTTP 요청 경로의 첫 번째 경로 요소(서버 이름 바로 뒤)로 지정됩니다. 첫 번째 경로 요소가 카탈로그의 RootId 속성과 일치하지 않으면 기본 카탈로그가 세션 카탈로그로 사용됩니다.

세션 카탈로그에서는 다음 세션 기본값을 제공합니다.

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>속성 </p> </th> 
   <th class="entry"> <p>주의 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 재료 데이터 파일의 루트 경로 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::VignettePath</span> </p> </td> 
   <td> <p> 비네팅 파일의 루트 경로 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::IccProfileRgb</span> </p> </td> 
   <td> <p> 비네트가 ICC 프로파일을 포함하지 않는 경우 기본 작업 색상 공간 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> 의 상대 HTTP 파일 경로에 대한 루트 URL <span class="codeph"> src=</span> 명령 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::ShowOverlapObjects</span> </p> </td> 
   <td> <p> 중복 객체에 대한 초기 표시/숨기기 상태 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::만료</span> </p> </td> 
   <td> <p> 프록시 서버 및 브라우저 캐시에 대한 회신 이미지의 Time-to-Live 값 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::MaxPix</span> </p> </td> 
   <td> <p> 허용되는 최대 회신 이미지 너비와 높이 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> 에 대한 기본값 <span class="codeph"> wid=</span> 및 <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::형식</span> </p> </td> 
   <td> <p> 기본값은 입니다. <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 특성::JpegQuality</span> </p> </td> 
   <td> <p> 기본값은 입니다. <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::TiffEncoding</span> </p> </td> 
   <td> <p> TIFF 이미지 출력에 대한 압축 유형 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 속성::선명 효과</span> </p> </td> 
   <td> <p> 기본값은 입니다. <span class="codeph"> 선명하게 하기=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> 다음 경우에 동작 지정 <span class="codeph"> sel=</span> 명령 실패 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> 다음 경우에 동작 지정 <span class="codeph"> obj=</span> 명령 실패 </p> </td> 
  </tr> 
 </tbody> 
</table>
