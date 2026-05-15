---
title: 비디오 플레이어 아이콘 효과
description: 재생 아이콘이 비디오 보기 영역에 오버레이됩니다. 비디오가 일시 중지되거나 비디오 끝에 도달하면 표시되며, 이는 iconeffect 매개 변수에도 달라집니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
TQID: 'https://experienceleague.adobe.com/LAq8JtRGEkPSrYm5QLGQz6RjhpSSxx7lQcbyaZsIhIw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 0%

---

# 비디오 플레이어 아이콘 효과{#video-player-icon-effect}

재생 아이콘이 비디오 보기 영역에 오버레이됩니다. 비디오가 일시 중지되거나 비디오 끝에 도달하면 표시되며, 이는 iconeffect 매개 변수에도 달라집니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생 아이콘의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
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
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
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

아이콘 효과는 `state` 특성 선택기를 지원합니다. 선택기 `state="play"`은(는) 재생 중에 비디오가 일시 중지된 경우에 사용되며 `state="replay"`은(는) 재생 헤드가 스트림 끝에 있는 경우에 사용됩니다.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

100 x 100픽셀 재생 아이콘을 설정합니다.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
