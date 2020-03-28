---
description: 이 단추를 클릭하거나 탭하면 기본 보기에서 이미지가 축소됩니다. 화면 공간을 절약하기 위해 휴대폰에는 이 단추가 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
seo-description: 이 단추를 클릭하거나 탭하면 기본 보기에서 이미지가 축소됩니다. 화면 공간을 절약하기 위해 휴대폰에는 이 단추가 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
seo-title: 축소 단추
solution: Experience Manager
title: 축소 단추
topic: Dynamic media
uuid: edc46e24-d3d9-4d1e-8676-ec441936458d
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom out button{#zoom-out-button}

이 단추를 클릭하거나 탭하면 기본 보기에서 이미지가 축소됩니다. 화면 공간을 절약하기 위해 휴대폰에는 이 단추가 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7zoomoutbutton
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
   <td colname="col2"> <p>패딩 등 오른쪽 테두리에서 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩 등 왼쪽 테두리에서 위치를 지정할 수 있습니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 속성 선택기를 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 [내용은 사용자 인터페이스 요소의](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 현지화를 참조하십시오.

예 - 32 x 32픽셀의 축소 단추를 설정하고 뷰어의 위쪽 및 오른쪽 가장자리에서 6픽셀을 배치하고 서로 다른 4개의 단추 상태에 대해 다른 이미지를 표시하려면

```
.s7mixedmediaviewer .s7zoomoutbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```

