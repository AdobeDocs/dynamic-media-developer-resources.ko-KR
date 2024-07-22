---
title: Video360Player.posterimage
description: Video360 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: fffd0976-0aeb-4e61-981f-b84e9076f35f
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# Video360Player.posterimage{#video-player-posterimage}

Video360 뷰어에 대한 구성 속성입니다.

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">개 없음|[?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 포스터 이미지 모양을 제어하는 이미지 제공 수정자입니다. URL에 지정되는 경우 HTTP 인코딩은 다음과 같습니다. </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?<span class="codeph"> %3F</span>(으)로 </span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span>(<span class="codeph"> %26</span>) </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span>(으)로 <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p> 이 수정자는 Dynamic Media Classic 또는 Adobe Experience Manager(Dynamic Media)에서 호스팅되는 비디오 컨텐츠에 사용됩니다. </p> <p>기본 포스터 이미지가 표시되지 않도록 하려면 <span class="codeph"> none</span>을(를) 포스터 이미지 값으로 지정하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

없음.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
