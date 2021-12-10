---
title: 전체 화면 단추
description: 사용자가 선택할 때 뷰어가 전체 화면 모드로 들어가거나 종료되도록 합니다. 뷰어가 팝업 모드에서 작동하며 시스템이 기본 전체 화면을 지원하지 않는 경우에는 이 단추가 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bbbf32db-15ce-4273-acc0-b6725b5405fb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# 전체 화면 단추{#full-screen-button}

사용자가 선택할 때 뷰어가 전체 화면 모드로 들어가거나 종료되도록 합니다. 뷰어가 팝업 모드에서 작동하며 시스템이 기본 전체 화면을 지원하지 않는 경우에는 이 단추가 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7zoomviewer .s7fullscreenbutton
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
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 오른쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 왼쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 및 `selected` 속성 선택기를 사용하여 다른 스킨을 다른 단추 상태에 적용할 수 있습니다. 특히, `selected='true'` 는 &quot;전체 화면&quot; 상태에 해당하며 `selected='false'` 는 &quot;일반&quot; 상태에 해당합니다.

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

예 - 32 x 32픽셀인 전체 화면 단추를 설정하고 뷰어 상단 및 오른쪽 가장자리로부터 6픽셀을 배치합니다. 그리고 마지막으로, 선택 또는 선택되지 않은 경우 4개의 서로 다른 버튼 상태에 대해 다른 이미지가 표시됩니다.

```
.s7zoomviewer .s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7zoomviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7zoomviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7zoomviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7zoomviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7zoomviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7zoomviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7zoomviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7zoomviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
