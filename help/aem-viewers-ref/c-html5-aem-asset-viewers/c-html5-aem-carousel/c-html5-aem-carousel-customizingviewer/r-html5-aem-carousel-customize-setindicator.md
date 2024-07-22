---
title: 표시기 설정
description: 세트 표시기는 뷰어 하단에 렌더링된 일련의 점입니다. 세트 내의 현재 위치를 표시합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# 표시기 설정{#set-indicator}

세트 표시기는 뷰어 하단에 렌더링된 일련의 점입니다. 세트 내의 현재 위치를 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**집합 표시기의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 설정된 표시기 컨테이너의 모양이 제어됩니다.

```
.s7carouselviewer .s7setindicator
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
   <td colname="col2"> <p>설정 표시기의 16진수 형식 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>세트 표시기는 모드 속성 선택기를 지원하며, 이 선택기를 사용하여 점선 및 숫자 작업 모드에 대해 다양한 스타일을 적용할 수 있습니다. 특히 `mode="numeric"`은(는) 숫자 작업 모드에 해당하고 `mode="dotted"`은(는) 기본 점 상태에 해당합니다.

예를 들어 흰색 배경의 세트 표시기를 설정한다고 가정해 보겠습니다.

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

개별 세트 표시기 점의 모양은 CSS 클래스 선택기로 제어됩니다. 점선의 작업 모드와 숫자 작업 모드의 항목에 모두 적용됩니다.

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>설정된 표시기 점의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>설정된 표시점의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 여백(픽셀). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-상단 </span> </p> </td> 
   <td colname="col2"> <p>상단 여백(픽셀). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 여백(픽셀 단위). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-하단 </span> </p> </td> 
   <td colname="col2"> <p>아래 여백(픽셀). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>테두리 반경(픽셀). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>글꼴 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 수직 맞춤 </span> </p> </td> 
   <td colname="col2"> <p>배너 색인의 세로 정렬. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 줄 높이 </span> </p> </td> 
   <td colname="col2"> <p>배너 색인의 텍스트 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>지표 설정 항목은 `state` 특성 선택기를 지원하며, 이 선택기는 다른 썸네일 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히 `state="selected"`은(는) 집합의 현재 요소에 해당하고 `state="unselected"`은(는) 기본 항목 상태에 해당합니다.

예를 들어 데스크탑 시스템에 대해 세트 표시기를 점선 모드로 설정한다고 가정합니다. 뷰어 아래쪽에서 20픽셀 떨어진 위치에 배치하려고 합니다. 또한 선택하지 않은 점을 50%의 투명도와 15 x 15픽셀의 검정색으로 하고 7개의 픽셀은 둥근 모서리로 만듭니다. 선택한 점은 90% 투명도의 검정색이며, 18 x 18 픽셀이고 9개의 픽셀이 둥근 모서리입니다. 점 사이의 간격은 5픽셀입니다.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
