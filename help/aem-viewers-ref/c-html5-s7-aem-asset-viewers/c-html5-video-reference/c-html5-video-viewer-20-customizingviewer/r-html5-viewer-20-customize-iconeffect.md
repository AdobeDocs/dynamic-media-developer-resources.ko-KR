---
description: 재생 아이콘은 기본 보기 영역에 오버레이됩니다. 비디오가 일시 중지될 때 또는 비디오 끝에 도달할 때 표시되며 아이콘 효과 매개 변수도 달라집니다.
seo-description: 재생 아이콘은 기본 보기 영역에 오버레이됩니다. 비디오가 일시 중지될 때 또는 비디오 끝에 도달할 때 표시되며 아이콘 효과 매개 변수도 달라집니다.
seo-title: 아이콘 효과
solution: Experience Manager
title: 아이콘 효과
topic: Dynamic media
uuid: dcab487d-0bd6-4899-82e2-e29fa812a864
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Icon effect{#icon-effect}

재생 아이콘은 기본 보기 영역에 오버레이됩니다. 비디오가 일시 중지될 때 또는 비디오 끝에 도달할 때 표시되며 아이콘 효과 매개 변수도 달라집니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생 아이콘의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer . s7videoplayer .s7iconeffect
```

**재생 아이콘의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 재생 아이콘에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 재생 아이콘의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>재생 아이콘의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

아이콘 효과는 `state` 속성 선택기를 지원합니다. `state="play"` 재생이 진행되는 동안 비디오가 일시 중지될 때 사용되며 재생 헤드가 스트림 끝에 있을 `state="replay"` 때 사용됩니다.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

100 x 100픽셀 재생 아이콘을 설정합니다.

```
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

