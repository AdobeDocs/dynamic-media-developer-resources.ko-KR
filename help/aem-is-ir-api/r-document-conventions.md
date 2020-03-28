---
description: 이 문서에서는 다음 규칙을 사용합니다.
seo-description: 이 문서에서는 다음 규칙을 사용합니다.
seo-title: 문서 규칙
solution: Experience Manager
title: 문서 규칙
topic: Scene7 Image Serving - Image Rendering API
uuid: 049c4d1b-b363-43bd-9597-168c97884ab7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Document conventions{#document-conventions}

이 문서에서는 다음 규칙을 사용합니다.

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>리터럴 </p> </td> 
  <td class="stentry"> <p>구문 섹션에서 기울임체가 아닌 텍스트는 리터럴입니다.공백 및 기호 [ ] { } 에는 적용되지 않습니다.| *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>설명 부분에서는 작은 따옴표의 기울임체가 아닌 텍스트가 리터럴입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 매개 변수 </span> </p> </td> 
  <td class="stentry"> <p>기울임꼴은 실제 값으로 대체할 변수 또는 매개 변수를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> command= </span> </p> </td> 
  <td class="stentry"> <p>뒤에 '='가 있는 이름은 이미지 제공 HTTP 프로토콜 명령을 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 속성::Item </span> </p> </td> 
  <td class="stentry"> <p>다음 <span class="codeph"> 특성이 포함된 이름 접두어:이미지 카탈로그 속성을 </span> 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 카탈로그::항목 </span> </p> </td> 
  <td class="stentry"> <p>다음 <span class="codeph"> 카탈로그와 함께 접두사가 붙은 이름:이미지 카탈로그 데이터 필드를 </span> 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>다음 ICC가 접두사로 추가된 이름: <span class="codeph"> ICC 색상 프로필 맵의 필드를 </span> 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 글꼴::Item </span> </p> </td> 
  <td class="stentry"> <p>다음 <span class="codeph"> 글꼴이 접두사로 붙은 이름:글꼴 맵의 필드를 </span> 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 매크로:항목 </span> </p> </td> 
  <td class="stentry"> <p>매크로 접두사가 <span class="codeph"> 있는 이름:매크로 정의 테이블의 필드를 </span> 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 규칙 세트::항목 </span> </p> </td> 
  <td class="stentry"> <p>규칙 <span class="codeph"> 세트가 있는 이름:URL 사전 처리 규칙 세트의 요소를 </span> 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 기본값::Item </span> </p> </td> 
  <td class="stentry"> <p>다음 <span class="codeph"> 기본값으로 접두사가 붙은 이름:기본 이미지 카탈로그의 속성을 </span> 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [ <span class="varname"> 선택 </span>] </span> </p> </td> 
  <td class="stentry"> <p>선택적 구문 요소는 대괄호로 묶입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[ <span class="varname"> 선택 </span>사항] </span> </p> </td> 
  <td class="stentry"> <p>선택적 구문 <span class="varname"> 요소는 </span> 반복되지 않거나 더 이상 반복될 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 항목1 </span>| <span class="varname"> 항목2 </span></span> </p> </td> 
  <td class="stentry"> <p>세로 막대는 왼쪽에 있는 단일 구문 항목 또는 오른쪽에 있는 항목이 사용될 수 있음을 나타냅니다. 정확하게 하나의 항목을 선택해야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> { <span class="varname"> group </span>} </span> </p> </td> 
  <td class="stentry"> <p>중괄호는 구문 요소를 그룹화하는 데 사용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> group </span>} </span> </p> </td> 
  <td class="stentry"> <p>그룹 내의 구문 요소를 한 번 이상 반복할 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>흰색 공간 </p> </td> 
  <td class="stentry"> <p>HTTP 요청에서는 공백(공백 또는 탭)을 사용할 수 없습니다. 이 문서에서는 명확성을 위해 구문 요소 간에 공백을 사용하는 경우가 있습니다. </p> </td> 
 </tr> 
</table>

