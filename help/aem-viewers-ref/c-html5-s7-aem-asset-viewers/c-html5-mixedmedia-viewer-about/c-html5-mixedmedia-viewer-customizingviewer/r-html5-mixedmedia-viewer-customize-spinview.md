---
title: 회전 보기
description: 기본 보기는 현재 에셋이 회전 집합일 때 회전 이미지로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# 회전 보기{#spin-view}

기본 보기는 현재 에셋이 회전 집합일 때 회전 이미지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 보기 영역의 모양이 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 회전 보기의 16진수 형식 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 회전 보기를 투명하게 만듭니다.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
