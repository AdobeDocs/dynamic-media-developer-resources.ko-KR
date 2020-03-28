---
description: 세트 표시기는 터치 장치에서 뷰어를 사용할 때 기본 색상 견본 위에 렌더링되는 점 시리즈입니다. 스크롤 단추를 사용할 수 없을 때 축소판의 페이지를 탐색할 수 있는 점을 보여줍니다.
seo-description: 세트 표시기는 터치 장치에서 뷰어를 사용할 때 기본 색상 견본 위에 렌더링되는 점 시리즈입니다. 스크롤 단추를 사용할 수 없을 때 축소판의 페이지를 탐색할 수 있는 점을 보여줍니다.
seo-title: 표시기 설정
solution: Experience Manager
title: 표시기 설정
topic: Dynamic media
uuid: e62fac7c-28b6-40bf-83cc-8bcfbaa0dfa3
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 표시기 설정{#set-indicator}

세트 표시기는 터치 장치에서 뷰어를 사용할 때 기본 색상 견본 위에 렌더링되는 점 시리즈입니다. 스크롤 단추를 사용할 수 없을 때 축소판의 페이지를 탐색할 수 있는 점을 보여줍니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**세트 표시기의 CSS 속성**

세트 표시기 컨테이너의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>세트 표시기의 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 흰색 배경으로 세트 표시기를 설정하려면

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
   <td colname="col2"> <p>세트 표시기의 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>세트 표시기 점의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 여백(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>위쪽 여백(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 여백 </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 여백(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>하단 여백(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>테두리 반경(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>세트 표시기 점은 `state` 속성 선택기를 지원합니다. 이 선택기는 다른 축소판 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히 `state="selected"` 축소판의 현재 페이지에 해당하며 `state="unselected"` 기본 점 상태에 해당합니다.

예 - 세트 표시기 점을 15 x 15픽셀로 설정하려면, 두 개의 가로 여백, 5픽셀의 위쪽 여백, 1픽셀의 아래쪽 여백, 12픽셀 반경, #D5D3D3 기본 색상 및 #93933 활성 색상:

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

