---
description: 이 문서에서는 다음 규칙을 사용합니다.
solution: Experience Manager
title: 문서 규칙
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e93de3fa-dde1-4d79-93aa-9ad800840cfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# 문서 규칙{#document-conventions}

이 문서에서는 다음 규칙을 사용합니다.

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>리터럴 </p> </td> 
  <td class="stentry"> <p>구문 섹션에서 기울임체가 아닌 텍스트는 리터럴입니다. 이 규칙은 공백 및 기호 [ ] { }에는 적용되지 않습니다. | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'리터럴' </p> </td> 
  <td class="stentry"> <p>설명 섹션에서 작은 따옴표로 묶인 기울임체가 아닌 텍스트는 리터럴입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 매개 변수 </span> </p> </td> 
  <td class="stentry"> <p>기울임꼴 은 변수나 매개 변수가 실제 값으로 대체되는 것을 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 명령= </span> </p> </td> 
  <td class="stentry"> <p>후행 '='가 있는 이름은 이미지 제공 HTTP 프로토콜 명령을 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 특성::항목 </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 특성 접두사가 있는 이름: </span>이(가) 이미지 카탈로그 특성을 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 카탈로그::항목 </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그 접두사가 있는 이름: </span>이(가) 이미지 카탈로그 데이터 필드를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::항목 </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> icc:: </span>이(가) 접두사로 붙은 이름이 ICC 색상 프로파일 맵의 필드를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::Item </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 글꼴 접두사가 있는 이름: </span>은(는) 글꼴 맵의 필드를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 매크로:: 항목 </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 매크로:: </span> 접두사가 있는 이름이 매크로 정의 테이블의 필드를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 규칙 집합::항목 </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 규칙 집합: </span> 접두사가 있는 이름은 URL 사전 처리 규칙 집합의 요소를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 기본값::항목 </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 기본값이 접두사로 추가된 이름: </span>이(가) 기본 이미지 카탈로그의 특성을 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [ <span class="varname"> 선택적 </span>] </span> </p> </td> 
  <td class="stentry"> <p>선택적 구문 요소는 대괄호로 묶습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[ <span class="varname"> 선택적 </span>] </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> 선택적 </span> 구문 요소는 한 번 이상 반복될 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 항목1 </span>| <span class="varname"> 항목2 </span> </span> </p> </td> 
  <td class="stentry"> <p>세로 막대는 왼쪽에 있는 단일 구문 항목 또는 오른쪽에 있는 항목을 사용할 수 있음을 나타냅니다. 정확히 하나의 항목을 선택해야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> { <span class="varname"> 그룹 </span>} </span> </p> </td> 
  <td class="stentry"> <p>중괄호는 구문 요소를 그룹화하는 데 사용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> 그룹 </span>} </span> </p> </td> 
  <td class="stentry"> <p>그룹 내의 구문 요소들은 1회 이상 반복될 수 있다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>공백 </p> </td> 
  <td class="stentry"> <p>HTTP 요청에는 공백(공백 또는 탭)을 사용할 수 없습니다. 이 문서는 명확성을 위해 종종 구문 요소 사이의 공백을 사용합니다. </p> </td> 
 </tr> 
</table>
