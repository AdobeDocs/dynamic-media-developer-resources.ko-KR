---
title: 색상 견본
description: 색상 견본은 왼쪽 및 오른쪽에 선택적 스크롤 버튼이 있는 일련의 썸네일 이미지로 구성됩니다. 모든 썸네일이 컨테이너 너비에 맞지 않는 경우에만 스크롤 단추가 데스크탑에 표시됩니다. 모바일 장치에서 또는 썸네일이 컨테이너 너비에 맞을 수 있는 경우 스크롤 버튼이 표시되지 않습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 7eaa4a6e-98e8-477b-9f45-66f8a79dfd85
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 3%

---

# 색상 견본{#swatches}

색상 견본은 왼쪽 및 오른쪽에 선택적 스크롤 버튼이 있는 일련의 썸네일 이미지로 구성됩니다. 모든 썸네일이 컨테이너 너비에 맞지 않는 경우에만 스크롤 단추가 데스크탑에 표시됩니다. 모바일 장치에서 또는 썸네일이 컨테이너 너비에 맞을 수 있는 경우 스크롤 버튼이 표시되지 않습니다.

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 견본 컨테이너의 모양이 제어됩니다.

```
.s7zoomviewer .s7zoomresetbutton
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>견본의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>견본의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 컨테이너를 기준으로 한 세로 견본 오프셋입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 견본을 460 x 100픽셀로 설정합니다.

```
.s7zoomviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

견본 썸네일 간의 간격은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7zoomviewer .s7swatches .s7thumbcell`

<table id="table_565B354FEA814804A0BE3978E1242110"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 각 썸네일 주변의 가로 및 세로 여백 크기입니다. 실제 썸네일 간격은 다음에 대해 설정된 왼쪽 및 오른쪽 여백의 합계와 같습니다. <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**

가로 및 세로 간격을 모두 10픽셀로 설정합니다.

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

개별 썸네일의 모양은 다음 CSS 클래스 선택기로 제어합니다.

`.s7zoomviewer .s7swatches .s7thumb`

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
   <td colname="col2"> <p>썸네일의 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>썸네일은 `state` 속성 선택기: 다른 썸네일 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히, `state="selected"` 는 현재 기본 보기에 표시된 이미지의 썸네일에 해당합니다. `state="default"` 은 나머지 썸네일에 해당합니다. `state="over"` 마우스를 가리킬 때 사용됩니다.

예 - 56 x 56픽셀인 썸네일을 설정하려면 밝은 회색의 기본 테두리와 어두운 회색의 선택된 테두리를 사용합니다.

```
.s7zoomviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7zoomviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7zoomviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

왼쪽 및 오른쪽 스크롤 단추의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

CSS 위쪽, 왼쪽, 아래쪽 및 오른쪽 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 로직은 뷰어를 자동으로 배치합니다.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기: 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. `up`, `down`, `over`, 및 `disabled`.

버튼 도구 팁은 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

예 - 56 x 56픽셀이며 각 상태에 대해 서로 다른 아트웍이 있는 스크롤 단추를 설정합니다.

```
.s7zoomviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
