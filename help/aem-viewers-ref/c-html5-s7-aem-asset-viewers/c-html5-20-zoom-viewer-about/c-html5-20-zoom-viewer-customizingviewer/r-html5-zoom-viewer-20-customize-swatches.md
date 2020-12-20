---
description: 견본은 왼쪽 및 오른쪽에 선택적인 스크롤 단추가 있는 일련의 축소판 이미지로 구성됩니다. 스크롤 단추는 모든 축소판이 컨테이너 너비에 맞지 않는 경우에만 데스크탑에서 볼 수 있습니다. 모바일 장치에서는 축소판이 컨테이너 폭에 들어갈 수 있는 경우에는 스크롤 단추가 표시되지 않습니다.
seo-description: 견본은 왼쪽 및 오른쪽에 선택적인 스크롤 단추가 있는 일련의 축소판 이미지로 구성됩니다. 스크롤 단추는 모든 축소판이 컨테이너 너비에 맞지 않는 경우에만 데스크탑에서 볼 수 있습니다. 모바일 장치에서는 축소판이 컨테이너 폭에 들어갈 수 있는 경우에는 스크롤 단추가 표시되지 않습니다.
seo-title: 견본
solution: Experience Manager
title: 견본
topic: Dynamic media
uuid: d44e775d-5253-4990-98a4-84ff50db09b9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 3%

---


# 견본{#swatches}

견본은 왼쪽 및 오른쪽에 선택적인 스크롤 단추가 있는 일련의 축소판 이미지로 구성됩니다. 스크롤 단추는 모든 축소판이 컨테이너 너비에 맞지 않는 경우에만 데스크탑에서 볼 수 있습니다. 모바일 장치에서는 축소판이 컨테이너 폭에 들어갈 수 있는 경우에는 스크롤 단추가 표시되지 않습니다.

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

견본 컨테이너의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col2"> <p>견본 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>견본 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 컨테이너를 기준으로 하는 세로 견본 오프셋입니다. </p> </td> 
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

견본 축소판 사이의 간격은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col2"> <p> 각 축소판을 둘러싼 가로 및 세로 여백의 크기입니다. 실제 축소판 간격은 <span class="codeph"> .s7thumbcell </span>에 설정된 왼쪽 및 오른쪽 여백의 합계와 같습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**

세로 및 가로 모두 10픽셀로 간격을 설정하려면

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

개별 축소판의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>축소판의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>축소판의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>축소판의 테두리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>축소판은 `state` 속성 선택기를 지원합니다. 이 선택기는 다른 축소판 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히, `state="selected"`은 현재 기본 보기에 표시된 이미지의 축소판에 해당하고, `state="default"`은 나머지 축소판에 해당하며, 마우스 가리키기에 `state="over"`가 사용됩니다.

예 - 56 x 56픽셀의 축소판을 설정하려면 밝은 회색의 기본 테두리와 어두운 회색을 선택한 테두리를 사용합니다.

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

왼쪽 및 오른쪽 스크롤 단추의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

CSS 위쪽, 왼쪽, 아래쪽 및 오른쪽 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 논리는 자동으로 위치를 지정합니다.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.`up`, `down`, `over` 및 `disabled`.

단추 도구 설명을 현지화할 수 있습니다. [사용자 인터페이스 요소 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 56 x 56픽셀이고 각 상태에 대해 서로 다른 아트웍을 갖는 스크롤 단추를 설정하는 방법입니다.

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

