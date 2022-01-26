---
title: 표시기 설정
description: 세트 표시기는 터치 장치에서 뷰어를 사용할 때 주 색상 견본 위에 렌더링되는 일련의 점입니다. 스크롤 단추를 사용할 수 없을 때 축소판 페이지를 탐색하는 데 점이 도움이 됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 표시기 설정{#set-indicator}

세트 표시기는 터치 장치에서 뷰어를 사용할 때 주 색상 견본 위에 렌더링되는 일련의 점입니다. 스크롤 단추를 사용할 수 없을 때 축소판 페이지를 탐색하는 데 점이 도움이 됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**설정된 표시기의 CSS 속성**

설정된 표시기 컨테이너의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7setindicator
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
   <td colname="col2"> <p>배경색(설정 표시기의 16진수 형식)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 흰색 배경을 사용하여 세트 표시기를 만들려면

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

개별 세트 표시기 점의 모양은 CSS 클래스 선택기로 제어됩니다.

`.s7mixedmediaviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>설정된 표시기 점의 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>설정된 표시기 점의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 여백 </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 여백(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 상단 </span> </p> </td> 
   <td colname="col2"> <p>위쪽 여백(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 순익 </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 여백(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 하단 </span> </p> </td> 
   <td colname="col2"> <p>아래쪽 여백(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 반경 </span> </p> </td> 
   <td colname="col2"> <p>테두리 반경(픽셀 단위). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>표시기 점은 `state` 속성 선택기. 다른 스킨을 다른 축소판 상태에 적용하는 데 사용할 수 있습니다. 특히, `state="selected"` 축소판의 현재 페이지에 해당합니다. `state="unselected"` 는 기본 점 상태에 해당합니다.

예 - 15 x 15픽셀인 세트 표시기 점을 만들려면 두 픽셀 가로 여백, 5픽셀 위쪽 여백, 1픽셀 아래쪽 여백, 12픽셀 반경, #D5D3D3 기본 색상 및 #939393 활성 색상을 사용합니다.

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
