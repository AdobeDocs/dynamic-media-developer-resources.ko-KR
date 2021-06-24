---
description: 재생 아이콘은 기본 보기 영역에 겹쳐집니다. 비디오가 일시 중지되거나 비디오 끝에 도달하면 표시되며, iconeffect 매개 변수에도 적용됩니다.
solution: Experience Manager
title: 아이콘 효과
feature: Dynamic Media Classic,Viewers,SDK/API,비디오
role: Developer,Business Practitioner
exl-id: f4bf343a-4a78-470b-abe5-94e2d608f45d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# 아이콘 효과{#icon-effect}

재생 아이콘은 기본 보기 영역에 겹쳐집니다. 비디오가 일시 중지되거나 비디오 끝에 도달하면 표시되며, iconeffect 매개 변수에도 적용됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생 아이콘의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer . s7videoplayer .s7iconeffect
```

**재생 아이콘의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p> 재생 아이콘에 대해 표시된 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
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

아이콘 효과는 `state` 속성 선택기를 지원합니다. `state="play"` 재생 중에 비디오가 일시 중지될 때 사용되며 재생 헤드 `state="replay"` 가 스트림 끝에 있을 때 사용됩니다.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

100 x 100 픽셀 재생 아이콘을 설정합니다.

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
