---
title: 재생/일시 중지 단추
description: 재생/일시 중지 버튼은 사용자가 비디오 콘텐츠를 클릭할 때 비디오 플레이어에서 비디오 콘텐츠를 재생하거나 일시 중지하도록 합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: bbf34037-b571-4dc9-be52-070aef014c31
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---

# 재생/일시 중지 단추{#play-pause-button}

재생/일시 중지 버튼은 사용자가 비디오 콘텐츠를 클릭할 때 비디오 플레이어에서 비디오 콘텐츠를 재생하거나 일시 중지하도록 합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

CSS별로 버튼의 크기를 조정하고, 스킨을 지정하고, 버튼이 포함된 컨트롤 막대를 기준으로 버튼의 위치를 지정할 수 있습니다.

다음 CSS 클래스 선택기는 단추의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7playpausebutton
```

## 재생/일시 중지 버튼의 CSS 속성 {#css-properties-of-the-play-pause-button}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 오른쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 왼쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 아래쪽 테두리에서 위치합니다. </p> </td> 
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
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state`, `selected`, 및 `replay` 속성 선택기 : 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히, `selected='true'` 는 &quot;재생&quot; 상태에 해당하며 `selected='false'` 은 &quot;일시 중지&quot; 상태에 해당합니다.
>
>속성 `replay='true'` 비디오가 끝에 도달하고 버튼을 선택하면 처음부터 재생이 다시 시작됩니다.

단추 도구 설명을 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

32x32픽셀로, 컨트롤 막대의 위쪽 및 왼쪽 가장자리에서 6픽셀로 배치된 재생/일시 중지 단추를 설정합니다. 그리고 마지막으로, 선택하거나 선택하지 않았을 때 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시합니다.

```
.s7interactivevideoviewer .s7playpausebutton { 
top:6px; 
left:6px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][state='up'] { 
background-image:url(images/playBtn_up.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/pauseBtn_disabled.png); } 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/replayBtn_up.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][replay='true'][state='over'] {  
background-image:url(images/replayBtn_over.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][replay='true'][state='down'] {  
background-image:url(images/replayBtn_down.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/replayBtn_disabled.png); 
}
```
