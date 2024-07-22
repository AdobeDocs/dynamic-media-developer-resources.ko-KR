---
title: 기본 견본
description: 기본 색상 견본은 왼쪽 및 오른쪽에 선택적 스크롤 버튼이 있는 썸네일 이미지 행으로 구성됩니다. 모든 썸네일이 컨테이너의 너비에 맞지 않는 경우에만 스크롤 단추가 데스크탑에 표시됩니다. 모바일 장치에서 또는 썸네일이 컨테이너 너비에 맞을 수 있는 경우 스크롤 버튼이 표시되지 않습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e6ff32bf-f85a-4288-a0e5-34487229a9d9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# 기본 견본{#main-swatches}

기본 색상 견본은 왼쪽 및 오른쪽에 선택적 스크롤 버튼이 있는 썸네일 이미지 행으로 구성됩니다. 모든 썸네일이 컨테이너의 너비에 맞지 않는 경우에만 스크롤 단추가 데스크탑에 표시됩니다. 모바일 장치에서 또는 썸네일이 컨테이너 너비에 맞을 수 있는 경우 스크롤 버튼이 표시되지 않습니다.

색상 견본 컨테이너의 모양은 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7swatches
```

견본의 **CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>견본의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 컨테이너를 기준으로 오프셋된 수직 견본입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 100픽셀 높이의 색상 견본을 설정합니다.

```
.s7mixedmediviewer .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

견본 썸네일 간의 간격은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7mixedmediaviewer .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p> 각 썸네일 주변의 가로 및 세로 여백 크기입니다. 실제 썸네일 간격은 <span class="codeph"> .s7thumbcell </span>에 설정된 왼쪽 및 오른쪽 여백의 합계와 같습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**

가로 및 세로 간격을 모두 10픽셀로 설정합니다.

```
.s7mixedmediaviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

개별 썸네일의 모양은 다음 CSS 클래스 선택기로 제어합니다.

`.s7mixedmediaviewer .s7swatches .s7thumb`

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
   <td colname="col2"> <p>썸네일의 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>썸네일은 `state` 특성 선택기를 지원하며, 이 선택기를 사용하여 다른 썸네일 상태에 다른 스킨을 적용할 수 있습니다. 특히 `state="selected"`은(는) 현재 기본 보기에 표시된 이미지의 썸네일에 해당하고, `state="default"`은(는) 나머지 썸네일에 해당하며, `state="over"`은(는) 마우스 가리키기에 사용됩니다.

예 - 56 x 56픽셀인 썸네일을 설정하려면 밝은 회색의 기본 테두리와 어두운 회색의 선택된 테두리를 사용합니다.

```
.s7mixedmediaviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

에셋 유형은 썸네일 이미지 위에 오버레이되는 아이콘으로 표시되며, 다음 CSS 클래스 선택기로 제어됩니다.

`.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay`

<table id="table_460FC57D12CC4B52B3782F4DFAC3A194"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 오버레이의 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 오버레이의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

오버레이는 가능한 값 `image`(단일 이미지의 경우), `swatchset`(견본 세트의 경우), `spinset`(스핀 세트의 경우) 및 `video`(단일 비디오 또는 응용 비디오 세트의 경우)으로 `type` 특성 선택기를 지원합니다.

예 - 스핀 세트, 견본 세트 및 비디오에 대한 아이콘 오버레이를 설정하려면 다음을 수행합니다.

```
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="swatchset"] { 
 background-image: url(images/v2/ThumbOverlaySwatchSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="spinset"] { 
 background-image: url(images/v2/ThumbOverlaySpinSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="video"] { 
 background-image: url(images/v2/ThumbOverlayVideo.png);  
}
```

왼쪽 및 오른쪽 스크롤 단추의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7mixedmediaviewer .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7swatches .s7scrollrightbutton`

CSS `top`, `left`, `bottom` 및 `right` 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 로직은 뷰어를 자동으로 배치합니다.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 `up`, `down`, `over` 및 `disabled` 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

버튼 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)를 참조하십시오.

예 - 56 x 56픽셀이며 각 상태에 대해 서로 다른 아트웍이 있는 스크롤 단추를 설정합니다.

```
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
