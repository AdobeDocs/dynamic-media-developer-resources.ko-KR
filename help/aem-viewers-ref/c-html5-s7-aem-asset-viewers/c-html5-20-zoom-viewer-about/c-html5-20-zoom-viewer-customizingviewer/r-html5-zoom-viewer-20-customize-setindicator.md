---
description: 세트 표시기는 뷰어를 터치 장치에서 사용할 때 견본 위에 렌더링되는 일련의 점입니다. 스크롤 단추를 사용할 수 없을 때 이 점을 사용하면 축소판 페이지를 탐색할 수 있습니다.
seo-description: 세트 표시기는 뷰어를 터치 장치에서 사용할 때 견본 위에 렌더링되는 일련의 점입니다. 스크롤 단추를 사용할 수 없을 때 이 점을 사용하면 축소판 페이지를 탐색할 수 있습니다.
seo-title: 표시기 설정
solution: Experience Manager
title: 표시기 설정
topic: Dynamic media
uuid: 802916a6-cec5-469b-b54c-dd379925a8c2
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 1%

---


# 표시기{#set-indicator} 설정

세트 표시기는 뷰어를 터치 장치에서 사용할 때 견본 위에 렌더링되는 일련의 점입니다. 스크롤 단추를 사용할 수 없을 때 이 점을 사용하면 축소판 페이지를 탐색할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**세트 표시기의 CSS 속성**

설정된 표시기 컨테이너의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7zoomviewer .s7setindicator
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
   <td colname="col2"> <p>세트 표시기의 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 흰색 배경이 있는 설정 표시기를 설정하려면

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

개별 세트 표시기 점의 모양은 CSS 클래스 선택기로 제어됩니다.

`.s7zoomviewer .s7setindicator .s7dot`

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
   <td colname="col2"> <p>세트 표시기의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>설정된 표시기의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 여백  </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 여백(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽 여백  </span> </p> </td> 
   <td colname="col2"> <p>위쪽 여백(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 여백  </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 여백(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 하단  </span> </p> </td> 
   <td colname="col2"> <p>아래쪽 여백(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>테두리 반경(픽셀 단위). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>표시기 도트는 다른 축소판 상태에 다른 스킨을 적용하는 데 사용할 수 있는 `state` 속성 선택기를 지원합니다. 특히 `state="selected"`은 축소판의 현재 페이지에 해당하며, `state="unselected"`은 기본 도트 상태에 해당합니다.

예 - 설정 표시기 점을 15 x 15픽셀로 설정하려면 다음과 같이 2픽셀 가로 여백, 5픽셀 위쪽 여백, 1픽셀 아래쪽 여백, 12픽셀 반경, #D5D3D3 기본 색상 및 #939393 활성 색상을 사용합니다.

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```

