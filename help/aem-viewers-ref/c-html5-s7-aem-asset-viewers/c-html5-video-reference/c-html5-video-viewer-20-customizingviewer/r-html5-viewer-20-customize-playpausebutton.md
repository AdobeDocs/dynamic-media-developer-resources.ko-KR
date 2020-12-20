---
description: 재생/일시 정지 단추를 사용하면 사용자가 비디오 컨텐츠를 클릭할 때 비디오 플레이어가 재생되거나 일시 정지됩니다.
seo-description: 재생/일시 정지 단추를 사용하면 사용자가 비디오 컨텐츠를 클릭할 때 비디오 플레이어가 재생되거나 일시 정지됩니다.
seo-title: 재생/일시 정지 단추
solution: Experience Manager
title: 재생/일시 정지 단추
topic: Dynamic media
uuid: b910a837-07ba-4e06-aee8-c22619ed0a92
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---


# 재생/일시 정지 단추{#play-pause-button}

재생/일시 정지 단추를 사용하면 사용자가 비디오 컨텐츠를 클릭할 때 비디오 플레이어가 재생되거나 일시 정지됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

CSS를 사용하여 단추가 포함된 컨트롤 막대를 기준으로 단추의 크기를 조정하고, 스킨을 지정하고 위치를 지정할 수 있습니다.

다음 CSS 클래스 선택기는 단추 모양을 제어합니다.

```
.s7videoviewer .s7playpausebutton
```

## 재생/일시 정지 단추 {#css-properties-of-the-play-pause-button} 의 CSS 속성

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같이 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같이 오른쪽 테두리에서 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같이 왼쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패딩과 같이 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있는 `state`, `selected` 및 `replay` 속성 선택기를 모두 지원합니다. 특히, `selected='true'`은 &quot;재생&quot; 상태에 해당하고 `selected='false'`은 &quot;일시 중지&quot; 상태에 해당합니다.
>
>`replay='true'` 이 설정은 비디오가 종료에 도달하고 단추를 클릭하면 처음부터 재생이 다시 시작될 때 설정됩니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)의 현지화를 참조하십시오.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

32 x 32픽셀인 재생/일시 정지 단추를 설정하려면컨트롤 막대의 위쪽과 왼쪽 가장자리에서 6픽셀의 위치가 지정되고, 선택되거나 선택되지 않은 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지가 표시됩니다.

```
.s7videoviewer .s7playpausebutton { 
top:6px; 
left:6px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7playpausebutton[selected='true'][state='up'] { 
background-image:url(images/playBtn_up.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7videoviewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7videoviewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7videoviewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
} 
.s7videoviewer .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/pauseBtn_disabled.png); } 
} 
.s7videoviewer .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/replayBtn_up.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][replay='true'][state='over'] {  
background-image:url(images/replayBtn_over.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][replay='true'][state='down'] {  
background-image:url(images/replayBtn_down.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/replayBtn_disabled.png); 
}
```

