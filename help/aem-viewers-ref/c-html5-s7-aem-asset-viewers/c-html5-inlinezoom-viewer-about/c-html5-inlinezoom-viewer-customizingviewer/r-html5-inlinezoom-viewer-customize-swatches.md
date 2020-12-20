---
description: 견본은 왼쪽 및 오른쪽에 선택적인 스크롤 단추가 있는 일련의 축소판 이미지로 구성됩니다.
seo-description: 견본은 왼쪽 및 오른쪽에 선택적인 스크롤 단추가 있는 일련의 축소판 이미지로 구성됩니다.
seo-title: 견본
solution: Experience Manager
title: 견본
topic: Dynamic media
uuid: 92360088-7199-49c3-80ee-e175d234a78e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 3%

---


# 견본{#swatches}

견본은 왼쪽 및 오른쪽에 선택적인 스크롤 단추가 있는 일련의 축소판 이미지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

스크롤 단추는 모든 축소판이 컨테이너의 폭에 맞지 않는 경우에만 데스크탑에서 볼 수 있습니다. 모바일 장치에서는 축소판이 컨테이너 폭에 들어갈 수 있는 경우에는 스크롤 단추가 표시되지 않습니다.

**견본의 CSS 속성**

견본 컨테이너의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7swatches
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
   <td colname="col2"> <p> 견본 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>견본 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 뷰어 컨테이너를 기준으로 하는 세로 견본 오프셋입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 견본을 460 x 100픽셀로 설정하려면:

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**축소판 견본 간격의 CSS 속성**

견본 축소판 간의 간격은 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7swatches .s7thumbcell
```

<table id="table_70FAD50E38EB4647B8FAB832F552BBB8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 각 축소판을 둘러싼 가로 및 세로 여백의 크기입니다. 실제 축소판 간격은 <span class="codeph"> .s7thumbcell </span>에 대해 설정된 왼쪽 및 오른쪽 여백의 합과 같습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 세로 및 가로 모두 10픽셀로 간격을 설정하려면 다음을 수행합니다.

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**축소판 견본의 CSS 속성**

개별 축소판의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7swatches .s7thumb
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p> 축소판 견본의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>축소판 견본의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>축소판 견본 테두리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>축소판은 다른 축소판 상태에 다른 스킨을 적용하는 데 사용되는 `state` 속성 선택기를 지원합니다. 특히, `state="selected"`은 현재 기본 보기에 표시된 이미지의 축소판에 해당하고, `state="default"`는 나머지 축소판에 해당하며, 마우스 가리키기에 `state="over"`가 사용됩니다.

예 - 56 x 56픽셀의 축소판을 설정하고, 밝은 회색의 기본 테두리를 사용하고, 어두운 회색을 선택한 테두리를 설정하려면:

```
.s7flyoutviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7flyoutviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7flyoutviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

**왼쪽 및 오른쪽 스크롤 단추의 CSS 속성**

왼쪽 및 오른쪽 스크롤 단추의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

CSS `top`, `left`, `bottom` 및 `right` 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 논리는 자동으로 위치를 지정합니다.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 단추의 폭입니다. </p> </td> 
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
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#section-b0af39db1af74561aea9fddcc8cdc2c7" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 속성 선택기를 지원합니다. 이 선택기는 단추 상태 `up`, `down`, `over` 및 `disabled`에 다른 스킨을 적용하는 데 사용됩니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)의 현지화를 참조하십시오.

예 - 56 x 56픽셀이고 각 상태에 대해 서로 다른 아트웍을 포함하는 스크롤 단추를 설정하려면 다음과 같이 하십시오.

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

