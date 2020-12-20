---
description: 데스크톱 시스템에서는 단추와 같은 일부 사용자 인터페이스 요소에 마우스 가리키기에 표시되는 도구 설명이 있습니다.
seo-description: 데스크톱 시스템에서는 단추와 같은 일부 사용자 인터페이스 요소에 마우스 가리키기에 표시되는 도구 설명이 있습니다.
seo-title: 툴팁
solution: Experience Manager
title: 툴팁
topic: Dynamic media
uuid: a2717dfe-19f9-4295-bb9d-19b62139b176
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# 도구 설명{#tooltips}

데스크톱 시스템에서는 단추와 같은 일부 사용자 인터페이스 요소에 마우스 가리키기에 표시되는 도구 설명이 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

도구 설명의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7tooltip
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> 배경 테두리 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p> 배경 테두리 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 배경색. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>텍스트 글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>텍스트 글꼴 크기. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>포함 웹 페이지 내에서 도구 설명 스타일을 사용자 지정하는 경우 모든 속성에 `!IMPORTANT` 규칙이 포함되어야 합니다. 도구 설명이 뷰어의 CSS 파일에서 사용자 지정된 경우에는 필요하지 않습니다.

예 - 3px 모퉁이 반경, 검정 배경 및 Arial로 작성된 흰색 텍스트가 11픽셀인 회색 테두리가 있는 도구 설명을 설정하려면:

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```

