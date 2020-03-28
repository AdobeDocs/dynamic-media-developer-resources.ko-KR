---
description: 기본 보기는 배너 이미지로 구성됩니다.
seo-description: 기본 보기는 배너 이미지로 구성됩니다.
seo-title: 회전판 보기
solution: Experience Manager
title: 회전판 보기
topic: Dynamic media
uuid: bf2065cc-fef2-4d4e-ab2a-a533fa063a80
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 회전판 보기{#carousel-view}

기본 보기는 배너 이미지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7carouselviewer .s7carouselview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 기본 보기를 투명하게 만듭니다.

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```

