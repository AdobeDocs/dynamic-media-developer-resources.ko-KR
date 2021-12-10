---
title: 닫기 단추
description: 이 단추를 선택하거나 탭하면 포함된 웹 페이지가 닫힙니다. 이 단추는 closebutton 매개 변수가 1로 설정된 경우에만 나타납니다. CSS를 사용하여 이 단추의 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8f466e8c-29a8-408d-97ae-e40043cb04e5
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 3%

---

# 닫기 단추{#close-button}

이 단추를 선택하거나 탭하면 포함된 웹 페이지가 닫힙니다. 이 단추는 closebutton 매개 변수가 1로 설정된 경우에만 나타납니다. CSS를 사용하여 이 단추의 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7zoomviewer .s7closebutton
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
>이 버튼은 `state` 속성 선택기. 다른 스킨을 다른 단추 상태에 적용하는 데 사용할 수 있습니다.

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

예 - 32 x 32픽셀인 닫기 단추를 설정하고 뷰어 상단 및 오른쪽 가장자리로부터 6픽셀을 배치합니다. 마지막으로, 에서는 네 개의 서로 다른 단추 상태에 대해 다른 이미지를 표시합니다.

```
.s7zoomviewer .s7closebutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7zoomviewer .s7closebutton [state='up'] { 
background-image:url(images/v2/CloseButton_dark_up.png); 
} 
.s7zoomviewer .s7closebutton [state='over'] {  
background-image:url(images/v2/CloseButton_dark_over.png); 
} 
.s7zoomviewer .s7closebutton [state='down'] {  
background-image:url(images/v2/CloseButton_dark_down.png); 
} 
.s7zoomviewer .s7closebutton [state='disabled'] { 
background-image:url(images/v2/CloseButton_dark_disabled.png); 
}
```
