---
description: 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoPlayer.posteimage
solution: Experience Manager
title: VideoPlayer.posteimage
topic: Dynamic media
uuid: 59d81a72-ac17-4c32-ab47-89bd14dc17a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.posteimage{#videoplayer-posterimage}

비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 재생되기 전에 첫 번째 프레임에 표시할 이미지를 <span class="codeph"> serverurl</span>기준으로 해결했습니다. URL 파섹 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> %</span> 26 <span class="codeph"> 으로(&amp;A)</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> % <span class="codeph"> 3D</span> </p> </li> 
     </ul> </p> <p>image_id <span class="codeph"><span class="varname"></span></span> 값을 생략하면 구성 요소는 해당 자산에 대한 기본 포스터 이미지를 대신 사용하려고 합니다. </p> <p>비디오가 경로로 지정되면 기본 포스터 이미지 카탈로그 ID는 <span class="codeph"> catalog_id/image_id</span> 쌍으로 비디오 경로에서 파생됩니다. 여기서 <span class="codeph"> catalog_id</span> 는 <span class="codeph"> 경로의 첫 번째 토큰에 해당하며</span> image_id는확장자가 제거된 비디오의 이름입니다. 해당 ID를 가진 이미지가 없는 경우 포스터 이미지가 표시되지 않습니다. </p> <p>기본 포스터 이미지가 표시되지 않도록 하려면 <span class="codeph"> 없음을</span> 포스터 이미지 값으로 지정합니다. is <span class="codeph"><span class="varname"> Commands만</span></span> 지정된 경우 이미지가 표시되기 전에 기본 포스터 이미지에 명령이 적용됩니다. </p> </td> 
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

