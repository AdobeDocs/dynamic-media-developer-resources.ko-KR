---
title: 이미지 렌더링 HTTP 프로토콜 기본 구문
description: 이 섹션에서는 Dynamic Media 이미지 렌더링 HTTP 프로토콜의 기본 구문을 설명합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 4%

---

# 이미지 렌더링 HTTP 프로토콜 기본 구문{#image-rendering-http-protocol-basic-syntax}

이 섹션에서는 Dynamic Media 이미지 렌더링 HTTP 프로토콜의 기본 구문을 설명합니다.

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignett</span> ] [ ?<span class="varname"> 수정자</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 서버 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> 포트</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignett </span> </p> </td> 
   <td colname="col2"> <p>비네팅 지정자(상대 파일 경로 또는 비네팅 카탈로그 항목). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 수정자 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 수정자</span> *[ &amp; <span class="varname"> 수정자</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 수정자 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 명령</span> | { $ <span class="varname"> 매크로</span> $ } | { .<span class="varname"> 댓글</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 명령 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 매크로 </span> </p> </td> 
   <td colname="col2"> <p>명령 매크로의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 댓글 </span> </p> </td> 
   <td colname="col2"> <p>주석 문자열(서버에서 무시됨)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>명령 또는 속성의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>사용자 지정 변수의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value </span> </p> </td> 
   <td colname="col2"> <p>명령 또는 변수 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`*, 및 *`var`* 는 대/소문자를 구분하지 않습니다. 서버는 다른 모든 문자열 값의 대소문자를 유지합니다.

**서버 식별자**

&#39; `/ir/render`이미지 렌더링에 대한 모든 HTTP 요청에 &#39; 루트 컨텍스트가 필요합니다.

**설명**

주석은 어디에서나 요청 문자열에 포함될 수 있으며 마침표(.)로 식별됩니다. 명령 구분 기호(&amp;)의 바로 다음에 옵니다. 주석은 (인코딩되지 않은) 명령 구분 기호의 다음 발생에 의해 종료됩니다. 이 기능은 타임스탬프 및 데이터베이스 ID와 같이 이미지 제공 용이 아닌 요청에 정보를 추가하는 데 사용할 수 있습니다.

**HTTP 디코딩**

첫 번째 추출 이미지 렌더링 *`object`* 및 *`modifiers`* 수신 요청에서 다음 *`object`* 에서는 개별적으로 HTTP 디코딩된 경로 요소로 분리됩니다. 다음 *`modifiers`* 문자열은 *`command`*= *`value`* 쌍 및 *`value`* 그런 다음 HTTP 디코딩을 사용하여 명령별 처리 전에 처리합니다.
