---
description: 소스 이미지 속성입니다. URL 경로에 지정된 이미지 파일 또는 카탈로그 항목의 선택된 속성을 반환합니다.
seo-description: 소스 이미지 속성입니다. URL 경로에 지정된 이미지 파일 또는 카탈로그 항목의 선택된 속성을 반환합니다.
seo-title: imageprops
solution: Experience Manager
title: imageprops
topic: Scene7 Image Serving - Image Rendering API
uuid: e9bf2780-a520-4fb1-ab4c-40bb799e36a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# imageprops{#imageprops}

소스 이미지 속성입니다. URL 경로에 지정된 이미지 파일 또는 카탈로그 항목의 선택된 속성을 반환합니다.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>고유 요청 식별자. </p></td> 
 </tr> 
</table>

HTTP 응답은 `attribute::NonImgExpiration`을(를) 기준으로 TTL을 사용하여 액세스할 수 있습니다.

요청 문자열의 다른 명령은 무시됩니다.

JSONP 응답 형식을 지원하는 요청에서는 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.

다음 속성이 반환됩니다.

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> 속성</b> </td> 
   <td> <b> 유형</b> </td> 
   <td> <b> 설명</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> 카탈로그::</span> 앵커 또는 기본 기준점 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 이중 </p> </td> 
   <td> <p> <span class="codeph"> 카탈로그::</span> 만료 또는 기본 라이브 시간 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p>전체 해상도 이미지 높이(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 이 이미지와 연결된 프로필의 이름/설명 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 이미지. embeddedIccProfile</span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 연결된 프로필이 이미지에 포함된 경우 1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 이미지에 Photoshop 경로 데이터가 포함되어 있는 경우 1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 이미지. embeddedXmpData</span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 이미지에 XMP 데이터가 포함되어 있는 경우 1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 마스크가 없는 경우 0, 미리 곱하기 알파의 경우 1, 미리 곱하지 않은 알파의 경우 2, 별도의 마스크 이미지의 경우 3 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> <span class="codeph"> 카탈로그::카탈로그 항목이 </span> 아닌 경우 수정 또는 비어 있음 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 이미지. photoshopPathNames</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 이 이미지와 연관된 모든 Photoshop 경로의 이름 쉼표로 구분된 목록 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 이미지 유형, 'CMYK', 'RGB' 또는 'BW'일 수 있습니다(회색 비율 이미지의 경우). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> <span class="codeph"> 속성::</span> PostModifier 또는 카탈로그 항목이 아닌 경우 비어 있음 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> 기본 인쇄 해상도(픽셀/인치) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> <span class="codeph"> 카탈로그::</span> 해상도 또는 기본 개체 해상도 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p>수정 날짜/시간(<span class="codeph"> 카탈로그::TimeStamp</span> 또는 이미지 파일에서) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> <span class="codeph"> 카탈로그::</span> Thumb기본 축소판 해상도 리셀러 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> 카탈로그::</span> ThumbTypeor 기본 축소판 유형 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 전체 해상도 이미지 너비(픽셀) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 경로에 지정된 <span class="varname"> 개체</span>이(가) 확인되는 카탈로그 ID(<a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> 개체 ID 변환</a> 참조). </p> </td> 
  </tr> 
 </tbody> 
</table>

