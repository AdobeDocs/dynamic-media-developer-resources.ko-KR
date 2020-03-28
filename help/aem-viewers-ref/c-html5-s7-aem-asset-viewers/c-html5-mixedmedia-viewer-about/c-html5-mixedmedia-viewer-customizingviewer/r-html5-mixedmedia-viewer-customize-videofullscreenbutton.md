---
description: 사용자가 전체 화면 단추를 클릭하면 뷰어가 전체 화면 모드로 들어가거나 종료됩니다. 뷰어가 비디오를 표시하고 컨트롤 막대에 있는 경우에 사용됩니다. 뷰어가 팝업 모드에서 작동하고 시스템이 기본 전체 화면을 지원하지 않는 경우 이 단추가 표시되지 않습니다.
seo-description: 사용자가 전체 화면 단추를 클릭하면 뷰어가 전체 화면 모드로 들어가거나 종료됩니다. 뷰어가 비디오를 표시하고 컨트롤 막대에 있는 경우에 사용됩니다. 뷰어가 팝업 모드에서 작동하고 시스템이 기본 전체 화면을 지원하지 않는 경우 이 단추가 표시되지 않습니다.
seo-title: 비디오 전체 화면 단추
solution: Experience Manager
title: 비디오 전체 화면 단추
topic: Dynamic media
uuid: f264154b-eb4d-4dcb-b8c0-e06c383198ae
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 비디오 전체 화면 단추{#video-full-screen-button}

사용자가 전체 화면 단추를 클릭하면 뷰어가 전체 화면 모드로 들어가거나 종료됩니다. 뷰어가 비디오를 표시하고 컨트롤 막대에 있는 경우에 사용됩니다. 뷰어가 팝업 모드에서 작동하고 시스템이 기본 전체 화면을 지원하지 않는 경우 이 단추가 표시되지 않습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

전체 화면 단추의 크기를 CSS로 조정하고, 스킨 및 위치를, 전체 화면 단추를 포함하는 컨트롤 막대에 비례하여 지정할 수 있습니다.

전체 화면 단추의 모양은 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7fullscreenbutton
```

**전체 화면 단추의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 패딩 등 오른쪽 테두리에서 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 패딩 등 왼쪽 테두리에서 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 전체 화면 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>전체 화면 단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시된 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 및 `selected` 속성 선택기를 모두 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히, `selected='true'` &quot;전체 화면&quot; 상태에 해당하며 &quot;보통&quot; 상태에 `selected='false'` 해당합니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 [내용은 사용자 인터페이스 요소의](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 현지화를 참조하십시오.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

32 x 32픽셀의 전체 화면 단추를 설정하고 컨트롤 막대의 상단 및 오른쪽 가장자리에서 6픽셀을 배치합니다. 또한 선택되거나 선택하지 않을 때 4개의 서로 다른 단추 상태에 대해 다른 이미지를 표시합니다.

```
.s7mixedmediaviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

