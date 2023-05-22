---
title: SmartCropVideoPlayer.posterimage
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ff4f8e2c-b9c3-4fba-b3f0-fa1eaddcd8c0
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`: 명령`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|[<span class="varname"> image_id</span>][?<span class="varname"> : 명령</span>]</span> </p> </td> 
   <td colname="col2"> <p> 비디오 재생이 시작되기 전에 첫 번째 프레임에 표시할 이미지로, 확인 대상 <span class="codeph"> serverurl</span>. URL에 지정되는 경우 HTTP 인코딩은 다음과 같습니다. </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 다음으로: <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> 및</span> 다음으로: <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> 다음으로: <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>다음과 같은 경우 <span class="codeph"><span class="varname"> image_id</span></span> 값이 생략되면 구성 요소는 해당 에셋에 대한 기본 포스터 이미지를 대신 사용하려고 합니다. </p> <p>비디오가 경로로 지정되면 기본 포스터 이미지 카탈로그 ID가 비디오 경로에서 경로로 파생됩니다. <span class="codeph"> catalog_id/image_id</span> 짝을 지어 다음 <span class="codeph"> catalog_id</span> 은 경로의 첫 번째 토큰에 해당하며 <span class="codeph"> image_id</span> 는 확장이 제거된 비디오의 이름입니다. 해당 ID의 이미지가 없는 경우 포스터 이미지가 표시되지 않습니다. </p> <p>기본 포스터 이미지가 표시되지 않도록 하려면 <span class="codeph"> 없음</span> 포스터 이미지 값으로 사용됩니다. 다음과 같은 경우에만 <span class="codeph"><span class="varname"> : 명령</span></span> 이 옵션을 지정하면 이미지가 표시되기 전에 명령이 기본 포스터 이미지에 적용됩니다. </p> </td> 
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
