---
description: 이미지 카탈로그 속성입니다. 요청 경로에 지정된 이미지 카탈로그의 공통 특성을 반환합니다.
seo-description: 이미지 카탈로그 속성입니다. 요청 경로에 지정된 이미지 카탈로그의 공통 특성을 반환합니다.
seo-title: 카탈로그 속성
solution: Experience Manager
title: 카탈로그 속성
topic: Scene7 Image Serving - Image Rendering API
uuid: 09252d39-8604-4785-bcdc-ad229a691035
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# catalygprops{#catalogprops}

이미지 카탈로그 속성입니다. 요청 경로에 지정된 이미지 카탈로그의 공통 특성을 반환합니다.

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>고유 요청 식별자. </p></td> 
 </tr> 
</table>

카탈로그 ID를 생략하여 기본 카탈로그 속성( [!DNL default.ini])을 검색합니다. HTTP 응답은 `attribute::NonImgExpiration`을(를) 기준으로 TTL을 사용하여 액세스할 수 있습니다.

JSONP 응답 형식을 지원하는 요청에서는 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.

다음 속성 값이 반환됩니다.

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> 속성</b> </td> 
   <td> <b> 유형</b> </td> 
   <td> <b> 해당 카탈로그 속성</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> <span class="codeph"> 특성::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::defaultExt</span> </p> </td> 
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
   <td> <p> <span class="codeph"> 특성::만료</span> </p> </td> 
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
   <td> <p> <span class="codeph"> attribute::LastModified</span> 또는, 없는 경우  <span class="varname"> catalog</span><span class="filepath"> .</span> inifile의 마지막 수정시간 </p> </td> 
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
   <td> <p> <span class="codeph"> 속성::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> hex </p> </td> 
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
   <td> <p> <span class="codeph"> 카탈로그::워터마크</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> <span class="codeph"> 특성::워터마크</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

