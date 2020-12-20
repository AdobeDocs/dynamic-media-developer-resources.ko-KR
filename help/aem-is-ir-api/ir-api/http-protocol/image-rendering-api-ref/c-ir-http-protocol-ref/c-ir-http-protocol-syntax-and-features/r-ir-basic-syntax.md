---
description: 이 섹션에서는 Scene7 이미지 렌더링 HTTP 프로토콜의 기본 구문에 대해 설명합니다.
seo-description: 이 섹션에서는 Scene7 이미지 렌더링 HTTP 프로토콜의 기본 구문에 대해 설명합니다.
seo-title: 이미지 렌더링 HTTP 프로토콜 기본 구문
solution: Experience Manager
title: 이미지 렌더링 HTTP 프로토콜 기본 구문
topic: Scene7 Image Serving - Image Rendering API
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 3%

---


# 이미지 렌더링 HTTP 프로토콜 기본 구문{#image-rendering-http-protocol-basic-syntax}

이 섹션에서는 Scene7 이미지 렌더링 HTTP 프로토콜의 기본 구문에 대해 설명합니다.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>항목 </p> </th> 
   <th colname="col2" class="entry"> <p>정의 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 요청</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> 서버</span>/ir/render[/<span class="varname"> 비네팅</span> ] [ ?<span class="varname"> 수정자</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 서버 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [:<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 비네팅  </span> </p> </td> 
   <td colname="col2"> <p>비네팅 지정자(상대 파일 경로 또는 비네팅 카탈로그 항목). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 수정자 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 수정자</span> *[ &amp;  <span class="varname"> 수정자</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 수정자 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> 값</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 매크로  </span> </p> </td> 
   <td colname="col2"> <p>명령 매크로의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 주석  </span> </p> </td> 
   <td colname="col2"> <p>주석 문자열(서버에서 무시됨). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
   <td colname="col2"> <p>명령 또는 속성의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>사용자 지정 변수의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value  </span> </p> </td> 
   <td colname="col2"> <p>명령 또는 변수 값. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*,  *`cmdName`*&#x200B;및 대/소문자를 구분하지  *`macro`*  *`var`* 않습니다. 서버는 다른 모든 문자열 값의 대/소문자를 유지합니다.

**서버 식별자**

이미지 렌더링에 대한 모든 HTTP 요청에 대해 &#39; `/ir/render`&#39; 루트 컨텍스트가 필요합니다.

**설명**

주석은 어디에서나 요청 문자열에 포함될 수 있으며 마침표(.)로 식별됩니다. 명령 구분 문자(&amp;) 바로 뒤에 있습니다. 주석은 (인코딩되지 않은) 명령 구분 기호로 다음 항목으로 끝납니다. 이 기능은 타임스탬프, 데이터베이스 ID 등과 같이 이미지 제공 용이 아닌 요청에 정보를 추가하는 데 사용할 수 있습니다.

**HTTP 디코딩**

이미지 렌더링은 들어오는 요청에서 먼저 *`object`* 및 *`modifiers`*&#x200B;을 추출합니다. *`object`* 을 개별 HTTP 디코딩이 지정된 경로 요소로 분리됩니다. *`modifiers`* 문자열은 *`command`*= *`value`* 쌍으로 구분되고, *`value`*&#x200B;은 명령별 처리 전에 HTTP 디코딩됩니다.
