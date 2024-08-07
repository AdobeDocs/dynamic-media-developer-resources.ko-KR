---
title: 아이콘 효과
description: 재생 아이콘이 기본 보기 영역에 오버레이됩니다. 비디오가 일시 중지되거나 비디오 끝에 도달하면 표시되며, 이는 iconeffect 매개 변수에도 달라집니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# 아이콘 효과{#icon-effect}

재생 아이콘이 기본 보기 영역에 오버레이됩니다. 비디오가 일시 중지되거나 비디오 끝에 도달하면 표시되며, 이는 iconeffect 매개 변수에도 달라집니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생 아이콘의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7video360viewer . s7video360player .s7iconeffect
```

재생 아이콘의 **CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 재생 아이콘에 대해 표시된 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 재생 아이콘의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>재생 아이콘의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

아이콘 효과는 `state` 특성 선택기를 지원합니다. 속성 선택기 `state="play"`은(는) 재생 중에 비디오가 일시 중지된 경우에 사용되며 `state="replay"`은(는) 재생 헤드가 스트림 끝에 있는 경우에 사용됩니다.

**예** - 100 x 100픽셀 재생 아이콘을 설정합니다.

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
