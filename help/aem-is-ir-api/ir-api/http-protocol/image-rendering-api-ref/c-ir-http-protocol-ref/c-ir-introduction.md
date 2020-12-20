---
description: 이 문서에서는 Scene7 이미지 렌더링을 위한 HTTP 프로토콜을 설명합니다.
seo-description: 이 문서에서는 Scene7 이미지 렌더링을 위한 HTTP 프로토콜을 설명합니다.
seo-title: 소개
solution: Experience Manager
title: 소개
topic: Scene7 Image Serving - Image Rendering API
uuid: d709f1d2-e7cc-4e9f-b039-aa333e517cbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 2%

---


# 소개{#introduction}

이 문서에서는 Scene7 이미지 렌더링을 위한 HTTP 프로토콜을 설명합니다.

프로토콜의 공개적으로 사용 가능한 측면만 설명되어 있습니다. 서버는 Scene7 클라이언트 소프트웨어에서 사용하도록 예약된 추가 명령을 지원할 수 있습니다.

**대상**

이 문서는 웹 사이트 또는 사용자 정의 애플리케이션에 Scene7 이미지 렌더링을 활용하려는 숙련된 프로그래머 및 웹 사이트 개발자를 위해 작성되었습니다.

독자는 Scene7 이미지 작성 및 이미지 렌더링, 일반 HTTP 프로토콜 표준 및 규칙, 기본 이미지 용어에 익숙하다고 가정합니다.

**문서 규칙**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>리터럴 </p> </td> 
  <td class="stentry"> <p>구문 섹션에서 기울임체가 아닌 텍스트는 리터럴입니다.공백 및 기호 [ ] { }에는 적용되지 않습니다. | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>설명형 섹션에서 기울임체가 아닌 텍스트는 단일 인용 부호의 리터럴입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 매개 변수 </span> </p> </td> 
  <td class="stentry"> <p>기울임꼴은 실제 값으로 대체할 변수 또는 매개 변수를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 속성::Item  </span> </p> </td> 
  <td class="stentry"> <p>'attribute::'이 접두사로 붙은 이름은 이미지 카탈로그 특성을 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 카탈로그::Item  </span> </p> </td> 
  <td class="stentry"> <p>'catalog::'가 접두사로 붙은 이름은 재료 카탈로그 데이터 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>'icc::'가 접두사로 붙은 이름은 ICC 색상 프로파일 맵의 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 매크로::Item  </span> </p> </td> 
  <td class="stentry"> <p>'macro::'가 접두사로 붙은 이름은 매크로 정의 테이블의 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 규칙 세트::항목  </span> </p> </td> 
  <td class="stentry"> <p>'ruleset::'이 접두사로 붙은 이름은 URL 사전 처리 규칙 세트의 요소를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 기본값::Item  </span> </p> </td> 
  <td class="stentry"> <p>'default::'가 접두사로 붙은 이름은 기본 이미지 카탈로그의 특성을 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> 비네팅::항목  </span> </td> 
  <td class="stentry"> <p>'비네팅::'이 접두사로 붙은 이름은 비네팅 맵의 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> 옵션 </span> ] </p> </td> 
  <td class="stentry"> <p>선택적 구문 요소는 대괄호로 묶입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> 옵션 </span> ] </p> </td> 
  <td class="stentry"> <p>선택적 구문 요소를 반복하지 않거나 여러 번 반복할 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> item2  </span> </p> </td> 
  <td class="stentry"> <p>세로 막대는 왼쪽에 있는 단일 구문 항목이나 오른쪽에 있는 항목이 사용될 수 있음을 나타냅니다. 정확하게 하나의 항목을 선택해야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> 그룹 </span> } </p> </td> 
  <td class="stentry"> <p>중괄호는 구문 요소를 그룹화하는 데 사용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> 그룹 </span> } </p> </td> 
  <td class="stentry"> <p>그룹 내의 구문 요소를 한 번 이상 반복할 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>흰색 공간 </p> </td> 
  <td class="stentry"> <p>HTTP 요청에서는 공백(공백 또는 탭)을 사용할 수 없습니다. 이 문서에서는 명확성을 위해 구문 요소 사이의 공백을 사용하는 경우가 있습니다. </p> </td> 
 </tr> 
</table>

**일반 용어**

** *`MSS`* ** 자재 사양 세그먼트:요청에 있는 두 선택 명령 간의 재료 속성 집합.

** *`vignette`* ** 이미지 렌더링에 사용하기 위해 Scene7 이미지 작성에서 준비된 이미지입니다.
