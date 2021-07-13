---
description: 이 문서에서는 다음 규칙을 사용합니다.
solution: Experience Manager
title: 문서 규칙
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e93de3fa-dde1-4d79-93aa-9ad800840cfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 문서 규칙{#document-conventions}

이 문서에서는 다음 규칙을 사용합니다.

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>리터럴 </p> </td> 
  <td class="stentry"> <p>구문 섹션에서 기울임체가 아닌 텍스트는 리터럴입니다. 이 규칙은 공백 및 기호 [ ] { } 에는 적용되지 않습니다 | *. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> command=  </span> </p> </td> 
  <td class="stentry"> <p>후행 '='인 이름이 이미지 제공 HTTP 프로토콜 명령을 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 속성::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 특성이 접두사로 붙은 이름: </span>은(는) 이미지 카탈로그 속성을 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 카탈로그::항목  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그 접두사가 있는 이름: </span>은(는) 이미지 카탈로그 데이터 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::항목  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> icc 접두어가 있는 이름: </span>은 ICC 색상 프로필 맵의 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 글꼴이 접두사로 붙은 이름: </span> 은 글꼴 맵의 필드를 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 매크로: 항목  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 매크로 접두사가 있는 이름: </span> 은 매크로 정의 테이블의 필드를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 규칙 세트::항목  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 규칙 세트가 접두사로 붙은 이름: </span> 은 URL 사전 처리 규칙 세트의 요소를 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 기본값::항목  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 기본값 접두사가 있는 이름: </span> 은 기본 이미지 카탈로그의 속성을 참조합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [  <span class="varname"> 선택사항  </span>]  </span> </p> </td> 
  <td class="stentry"> <p>선택적 구문 요소는 대괄호로 묶입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[  <span class="varname"> 옵션  </span>]  </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> 선택적 </span> 구문 요소를 둘 이상 반복할 수 없습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 항목1  </span>|  <span class="varname"> item2  </span> </span> </p> </td> 
  <td class="stentry"> <p>세로 막대는 왼쪽에 있는 단일 구문 항목이나 오른쪽에 있는 항목을 사용할 수 있음을 나타냅니다. 정확히 하나의 항목을 선택해야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> {  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>구문 요소를 그룹화하는 데 중괄호가 사용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>그룹 내의 구문 요소를 한 번 이상 반복할 수 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>화이트 스페이스 </p> </td> 
  <td class="stentry"> <p>HTTP 요청에서는 공백(공백 또는 탭)을 사용할 수 없습니다. 이 문서는 명확성을 위해 구문 요소 사이에 공백을 사용하는 경우가 있습니다. </p> </td> 
 </tr> 
</table>
