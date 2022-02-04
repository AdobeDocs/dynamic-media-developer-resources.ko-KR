---
title: VideoPlayer.posterimage
description: 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 재생을 시작하기 전에 첫 번째 프레임에 표시할 이미지를 문제 해결했습니다 <span class="codeph"> serverurl</span>. URL에 지정된 경우 HTTP는 다음을 인코딩합니다. </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 로서의 <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> 로서의 <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> 로서의 <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>만약 <span class="codeph"><span class="varname"> image_id</span></span> 값이 생략되면 구성 요소는 해당 자산에 대한 기본 포스터 이미지를 대신 사용하려고 합니다. </p> <p>비디오가 경로로 지정되면 기본 포스터 이미지 카탈로그 ID는 비디오 경로에서 <span class="codeph"> catalog_id/image_id</span> 연결 위치 <span class="codeph"> catalog_id</span> 은 경로의 첫 번째 토큰에 해당합니다. 그리고, <span class="codeph"> image_id</span> 은 확장이 제거된 비디오 이름입니다. 해당 ID가 있는 이미지가 없는 경우 포스터 이미지가 표시되지 않습니다. </p> <p>기본 포스터 이미지가 표시되지 않도록 하려면 <span class="codeph"> 없음</span> 을 포스터 이미지 값으로 채우면 됩니다. 다음의 경우에만 <span class="codeph"><span class="varname"> isCommands</span></span> 이 지정되면 이미지가 표시되기 전에 기본 포스터 이미지에 명령이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

없음.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
