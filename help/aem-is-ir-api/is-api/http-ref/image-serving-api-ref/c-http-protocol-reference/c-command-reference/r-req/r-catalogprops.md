---
description: 이미지 카탈로그 속성. 요청 경로에 지정된 이미지 카탈로그의 공통 특성을 반환합니다.
solution: Experience Manager
title: catalogprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 4%

---

# catalogprops{#catalogprops}

이미지 카탈로그 속성. 요청 경로에 지정된 이미지 카탈로그의 공통 특성을 반환합니다.

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>고유 요청 식별자. </p></td> 
 </tr> 
</table>

기본 카탈로그 속성([!DNL default.ini])을 검색하려면 카탈로그 ID를 생략합니다. `attribute::NonImgExpiration`을(를) 기반으로 하는 TTL로 HTTP 응답을 캐시할 수 있습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`은(는) JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.

다음 속성 값이 반환됩니다.

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> 속성</b> </td> 
   <td> <b> 유형</b> </td> 
   <td> <b> 해당 카탈로그 특성</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> 16 </p> </td> 
   <td> <p> <span class="codeph"> 특성::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::defaultExt</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> <span class="codeph"> 특성::DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> 특성::DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> 특성::DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.expiration</span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> <span class="codeph"> 특성::Expiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> <span class="codeph"> 특성::DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> <span class="codeph"> 특성::NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> <span class="codeph"> 특성::LastModified</span> 또는 없는 경우 <span class="varname"> 카탈로그의 마지막 수정 시간</span><span class="filepath"> .ini</span> 파일 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> <span class="codeph"> 특성::JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> 특성::MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph"> 특성::PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> <span class="codeph"> 특성::PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> 특성::ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> <span class="codeph"> 특성::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> 16 </p> </td> 
   <td> <p> <span class="codeph"> 특성::ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> 특성::ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> <span class="codeph"> 특성::ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> 특성::ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> 특성::ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 카탈로그::watermark</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> <span class="codeph"> 특성::Watermark</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
