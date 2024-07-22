---
title: 전체 화면 단추
description: 전체 화면 버튼을 클릭하면 Smart Crop 비디오 플레이어가 전체 화면 모드로 전환되거나 종료됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 79b57f6d-17d2-48af-9414-b0ab9d24fbdc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# 전체 화면 단추{#full-screen-button}

전체 화면 버튼을 클릭하면 Smart Crop 비디오 플레이어가 전체 화면 모드로 전환되거나 종료됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

CSS별로 전체 화면 버튼의 크기를 조정하고, 스킨을 지정하고, 전체 화면 버튼을 포함하는 컨트롤 막대에 따라 배치할 수 있습니다.

전체 화면 버튼의 모양은 CSS 클래스 선택기로 제어됩니다.

```
.s7smartcropvideoviewer .s7fullscreenbutton
```

**전체 화면 단추의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 위쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 오른쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 남음 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 왼쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 아래쪽 테두리에서 위치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 전체 화면 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>전체 화면 버튼의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 버튼 상태에 대해 표시된 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 및 `selected` 특성 선택기를 모두 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히 `selected='true'`은(는) &quot;전체 화면&quot; 상태에 해당하고 `selected='false'`은(는) &quot;일반&quot; 상태에 해당합니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)를 참조하십시오.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

전체 화면 단추를 설정하려면 컨트롤 막대의 위쪽 및 오른쪽 가장자리에서 6픽셀을 32x32픽셀로 설정합니다. 또한 선택되거나 선택되지 않을 때 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시합니다.

```
.s7smartcropvideoviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
