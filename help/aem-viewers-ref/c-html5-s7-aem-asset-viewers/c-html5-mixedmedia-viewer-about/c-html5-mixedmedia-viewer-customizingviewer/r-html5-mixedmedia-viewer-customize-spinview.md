---
description: 기본 보기는 현재 자산이 스핀 세트일 때 스핀 이미지로 구성됩니다.
solution: Experience Manager
title: 회전 보기
feature: Dynamic Media Classic,뷰어,SDK/API,혼합 미디어 집합
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---


# 회전 보기{#spin-view}

기본 보기는 현재 자산이 스핀 세트일 때 스핀 이미지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 회전 보기 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 회전 보기를 투명하게 만듭니다.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

