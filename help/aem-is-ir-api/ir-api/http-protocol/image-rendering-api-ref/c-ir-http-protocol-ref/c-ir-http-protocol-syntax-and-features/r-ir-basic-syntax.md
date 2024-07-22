---
title: 이미지 렌더링 HTTP 프로토콜 기본 구문
description: 이 섹션에서는 Dynamic Media 이미지 렌더링 HTTP 프로토콜의 기본 구문에 대해 설명합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# 이미지 렌더링 HTTP 프로토콜 기본 구문{#image-rendering-http-protocol-basic-syntax}

이 섹션에서는 Dynamic Media 이미지 렌더링 HTTP 프로토콜의 기본 구문에 대해 설명합니다.

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> 비네팅</span> ] [ ?<span class="varname">개의 수정자</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 서버 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 비네팅 </span> </p> </td> 
   <td colname="col2"> <p>비네팅 지정자(상대 파일 경로 또는 비네팅 카탈로그 항목). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 수정자 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 한정자</span> *[ &amp; <span class="varname"> 한정자</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 한정자 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 명령</span> | { $ <span class="varname"> 매크로</span> $ } | { .<span class="varname"> 댓글</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 명령 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> 값</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 매크로 </span> </p> </td> 
   <td colname="col2"> <p>명령 매크로의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 댓글 </span> </p> </td> 
   <td colname="col2"> <p>주석 문자열(서버에서 무시됨). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>명령 또는 특성의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 변수 </span> </p> </td> 
   <td colname="col2"> <p>사용자 지정 변수의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 값 </span> </p> </td> 
   <td colname="col2"> <p>명령 또는 변수 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* 및 *`var`*&#x200B;은(는) 대/소문자를 구분하지 않습니다. 서버는 다른 모든 문자열 값의 대/소문자를 유지합니다.

**서버 식별자**

이미지 렌더링에 대한 모든 HTTP 요청에 &#39; `/ir/render`&#39; 루트 컨텍스트가 필요합니다.

**댓글**

주석은 어디에나 요청 문자열에 포함될 수 있으며 마침표(.)로 식별됩니다. 명령 구분 기호(&amp;)를 바로 뒤에 옵니다. (인코딩되지 않은) 명령 구분 기호가 다음에 발생할 때 설명이 종료됩니다. 이 기능은 타임스탬프 및 데이터베이스 ID와 같이, 이미지 제공용이 아닌 정보를 요청에 추가하는 데 사용할 수 있습니다.

**HTTP 디코딩**

이미지 렌더링은 먼저 들어오는 요청에서 *`object`* 및 *`modifiers`*&#x200B;을(를) 추출합니다. 그런 다음 *`object`*&#x200B;은(는) 개별적으로 HTTP 디코딩되는 경로 요소로 분리됩니다. *`modifiers`* 문자열은 *`command`*= *`value`* 쌍으로 분리되며, *`value`*&#x200B;은(는) 명령별 처리 전에 HTTP 디코딩됩니다.
