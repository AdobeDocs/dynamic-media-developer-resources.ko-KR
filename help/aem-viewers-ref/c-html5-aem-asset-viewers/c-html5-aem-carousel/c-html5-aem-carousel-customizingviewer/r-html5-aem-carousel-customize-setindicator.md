---
description: 세트 표시기는 뷰어 아래쪽에 렌더링된 일련의 점입니다. 세트 내의 현재 위치를 표시합니다.
seo-description: 세트 표시기는 뷰어 아래쪽에 렌더링된 일련의 점입니다. 세트 내의 현재 위치를 표시합니다.
seo-title: 표시기 설정
solution: Experience Manager
title: 표시기 설정
topic: Dynamic media
uuid: 3f90a216-654f-44a9-947d-592bd5f342d4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# 표시기{#set-indicator} 설정

세트 표시기는 뷰어 아래쪽에 렌더링된 일련의 점입니다. 세트 내의 현재 위치를 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**세트 표시기의 CSS 속성**

설정된 표시기 컨테이너의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>세트 표시기의 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>세트 표시기는 모드 속성 선택기를 지원하므로 점선과 숫자 작업 모드에 서로 다른 스타일을 적용할 수 있습니다. 특히 `mode="numeric"`은 숫자 작업 모드에 해당합니다.`mode="dotted"`은 기본 도트 상태에 해당합니다.

예 - 흰색 배경이 있는 설정 표시기를 설정하려면

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

개별 세트 표시기 점의 모양은 CSS 클래스 선택기로 제어됩니다. 점선 및 숫자 작업 모드의 항목에 적용됩니다.

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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴의 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>글꼴 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 수직 정렬  </span> </p> </td> 
   <td colname="col2"> <p>배너 인덱스의 세로 정렬입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 선 높이  </span> </p> </td> 
   <td colname="col2"> <p>배너 색인의 텍스트 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>표시기 항목을 설정하면 `state` 속성 선택기가 지원되며 이 선택기를 사용하여 다른 축소판 상태에 다른 스킨을 적용할 수 있습니다. 특히, `state="selected"`은 세트의 현재 요소에 해당합니다.`state="unselected"`은 기본 항목 상태에 해당합니다.

예 - 데스크톱 시스템의 점선 모드에서 설정 표시기를 설정하여 뷰어 아래쪽에서 20픽셀에 배치할 수 있습니다. 선택되지 않은 점은 50% 투명도가 있는 검정, 15 x 15픽셀, 7픽셀의 둥근 모퉁이가 있습니다. 선택한 점들은 90% 투명도가 있는 검정으로, 18 x 18픽셀과 9픽셀의 둥근 모퉁이로 구성됩니다. 점 사이의 간격은 5픽셀입니다.

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

