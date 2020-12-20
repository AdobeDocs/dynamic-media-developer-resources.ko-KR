---
description: Video360 뷰어에 대한 구성 속성입니다.
seo-description: Video360 뷰어에 대한 구성 속성입니다.
seo-title: Video360Player.posterimage
solution: Experience Manager
title: Video360Player.posterimage
topic: Dynamic media
uuid: a1adc3b7-2ea3-4f26-84f2-b5c2f4418038
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 14%

---


# Video360Player.posterimage{#video-player-posterimage}

Video360 뷰어에 대한 구성 속성입니다.

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 포스터 이미지 모양을 제어하는 이미지 제공 수정자입니다. URL에 지정된 경우 다음을 HTTP로 인코딩합니다. </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> </span> %26 <span class="codeph"> 으로(&amp;A)</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> = </span> %3D <span class="codeph"> 로</span> </p> </li> 
     </ul> </p> <p> 이 수정자는 Dynamic Media Classic 또는 AEM Dynamic Media에서 호스팅되는 비디오 컨텐츠에 대해 작동합니다. </p> <p>기본 포스터 이미지가 표시되지 않도록 하려면 포스터 이미지 값으로 <span class="codeph"> none</span>을 지정합니다. </p> </td> 
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

