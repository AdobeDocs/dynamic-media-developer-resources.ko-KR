---
description: HTTP 프로토콜 기본 구문은 다음과 같습니다.
solution: Experience Manager
title: 이미지 제공 HTTP 프로토콜 기본 구문
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# 이미지 제공 HTTP 프로토콜 기본 구문{#image-serving-http-protocol-basic-syntax}

HTTP 프로토콜 기본 구문은 다음과 같습니다.

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 요청</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> 수정자</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 서버 </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 개체</span> </span> </p></td> 
  <td class="stentry"> <p>Source 개체 지정자(이미지 경로 또는 이미지 카탈로그 항목)입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 수정자</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 수정자</span>*[&amp;<span class="varname"> 수정자</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 수정자</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">명령|{$<span class="varname"> 매크로</span>$}|&lbrace;<span class="varname">개의 댓글</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 명령</span> </span> </p> </td> 
  <td class="stentry"> <p>&lbrace;<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 매크로</span> </span> </p> </td> 
  <td class="stentry"> <p>명령 매크로의 이름입니다.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 댓글</span> </span> </p></td> 
  <td class="stentry"> <p>주석 문자열(서버에서 무시됨).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>지원되는 명령 또는 속성 이름 중 하나입니다.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>사용자 지정 변수의 이름입니다.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 값</span> </span> </p></td> 
  <td class="stentry"> <p>명령 또는 변수 값입니다. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`* 및 *`var`*&#x200B;은(는) 대/소문자를 구분하지 않습니다. 서버는 다른 모든 문자열 값의 대/소문자를 유지합니다.

*`value`*&#x200B;은(는) 명령에 따라 다르며 쉼표로 구분된 하나 이상의 값으로 구성될 수 있습니다. 자세한 내용은 개별 명령에 대한 설명을 참조하십시오.

## 서버 식별자 {#section-926ae55ddba14b8d952147a5fd701e14}

이미지 제공에 대한 모든 HTTP 요청에 [!DNL /is/image] 루트 컨텍스트가 필요합니다.

## HTTP 디코딩 {#section-20922baccd804d2d986b44ce9a183a7d}

이미지 제공에서 들어오는 요청에서 *`object`* 및 *`modifiers`*&#x200B;을(를) 먼저 추출합니다. 그런 다음 *`object`*&#x200B;은(는) 개별적으로 HTTP 디코딩되는 경로 요소로 분리됩니다. *`modifiers`* 문자열은 *`command`*= *`value`* 쌍으로 분리되며, *`value`*&#x200B;은(는) 명령별 처리 전에 HTTP 디코딩됩니다.

>[!NOTE]
>
>설명서에 별도로 언급되지 않는 한, 모든 안전하지 않은 문자는 HTTP 표준에 따라 인코딩해야 합니다. 자세한 내용은 HTTP 사양을 참조하십시오.

## 설명 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

주석은 어디에나 요청 문자열에 포함될 수 있으며 마침표(.)로 식별됩니다. 구분 기호(&amp;) 바로 다음에 옵니다. (인코딩되지 않은) 명령 구분 기호가 다음에 발생할 때 설명이 종료됩니다. 이 기능은 타임스탬프 및 데이터베이스 ID와 같이, 이미지 제공용으로 사용되지 않는 정보를 요청에 추가하는 데 사용할 수 있습니다.

## 참조 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[데이터 형식](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [HTTP/1.1 사양](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
