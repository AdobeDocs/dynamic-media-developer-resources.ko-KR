---
title: 소개
description: 이 문서에서는 Dynamic Media 이미지 렌더링에 대한 HTTP 프로토콜을 설명합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# 소개{#introduction}

이 문서에서는 Dynamic Media 이미지 렌더링에 대한 HTTP 프로토콜을 설명합니다.

프로토콜의 공개 가능한 측면만 설명되어 있습니다. 서버는 Dynamic Media 클라이언트 소프트웨어에서 사용하도록 예약된 추가 명령을 지원할 수 있습니다.

**대상**

이 문서는 웹 사이트 또는 사용자 지정 애플리케이션에 Dynamic Media 이미지 렌더링을 사용하려는 숙련된 프로그래머 및 웹 사이트 개발자를 위한 것입니다.

리더기는 Dynamic Media 이미지 작성 및 이미지 렌더링, 일반 HTTP 프로토콜 표준 및 규칙, 기본 이미징 용어에 익숙하다고 가정합니다.

**문서 규칙**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>리터럴 </p> </td> 
  <td class="stentry"> <p>구문 섹션에서 기울임체가 아닌 텍스트는 리터럴입니다. 공백 및 기호 [ ] { } 에는 적용되지 않습니다. | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>설명 섹션에서 기울임체가 아닌 텍스트는 작은 따옴표로 묶습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 매개 변수 </span> </p> </td> 
  <td class="stentry"> <p>기울임꼴 은 실제 값으로 대체될 변수 또는 매개 변수를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 속성::Item </span> </p> </td> 
  <td class="stentry"> <p>'attribute::' 접두사가 있는 이름은 이미지 카탈로그 속성을 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 카탈로그::항목 </span> </p> </td> 
  <td class="stentry"> <p>'catalog::'가 접두사로 붙은 이름은 재료 카탈로그 데이터 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::항목 </span> </p> </td> 
  <td class="stentry"> <p>'icc::'가 접두사로 붙은 이름은 ICC 색상 프로필 맵의 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 매크로::항목 </span> </p> </td> 
  <td class="stentry"> <p>'macro::' 접두사가 있는 이름은 매크로 정의 테이블의 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 규칙 세트::항목 </span> </p> </td> 
  <td class="stentry"> <p>'규칙 세트::'가 접두사로 붙은 이름은 URL 사전 처리 규칙 세트의 요소를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 기본값::항목 </span> </p> </td> 
  <td class="stentry"> <p>'default::' 접두사가 있는 이름은 기본 이미지 카탈로그의 속성을 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> 비네팅::항목 </span> </td> 
  <td class="stentry"> <p>'vignette::' 접두사가 있는 이름이 비네팅 맵의 필드를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> 옵션 </span> ] </p> </td> 
  <td class="stentry"> <p>선택적 구문 요소는 대괄호로 묶입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> 옵션 </span> ] </p> </td> 
  <td class="stentry"> <p>선택적 구문 요소를 두 번 이상 반복하지 않을 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 항목1 </span>| <span class="varname"> 품목2 </span> </p> </td> 
  <td class="stentry"> <p>세로 막대는 왼쪽에 있는 단일 구문 항목이나 오른쪽에 있는 항목이 사용될 수 있음을 나타냅니다. 정확히 하나의 항목을 선택해야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> 그룹 </span> } </p> </td> 
  <td class="stentry"> <p>구문 요소를 그룹화하는 데 중괄호가 사용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> 그룹 </span> } </p> </td> 
  <td class="stentry"> <p>그룹 내의 구문 요소를 한 번 이상 반복할 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>화이트 스페이스 </p> </td> 
  <td class="stentry"> <p>HTTP 요청에서는 공백(공백 또는 탭)을 사용할 수 없습니다. 이 문서는 명확성을 위해 구문 요소 간의 공백을 사용하는 경우가 있습니다. </p> </td> 
 </tr> 
</table>

**공통 용어**

** *`MSS`* ** 자재 사양 세그먼트: 요청에서 두 선택 명령 사이의 재료 속성 집합입니다.

** *`vignette`* ** 이미지 렌더링에 사용하기 위해 Dynamic Media 이미지 작성에서 준비된 이미지입니다.
