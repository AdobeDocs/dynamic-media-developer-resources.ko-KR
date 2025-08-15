---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 비디오 재생이 시작되기 전에 첫 번째 프레임에 표시할 이미지로, <span class="codeph"> serverurl</span>에 대해 확인됩니다. URL에 지정되는 경우 HTTP 인코딩은 다음과 같습니다. </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> %3F<span class="codeph">(으)로 </span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span>(<span class="codeph"> %26</span>) </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span>(으)로 <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p><span class="codeph"><span class="varname"> image_id</span></span> 값이 생략된 경우 구성 요소는 해당 자산에 대한 기본 포스터 이미지를 대신 사용하려고 합니다. </p> <p>비디오가 경로로 지정되면 기본 포스터 이미지 카탈로그 ID가 비디오 경로에서 <span class="codeph"> catalog_id/image_id</span> 쌍으로 파생됩니다. 여기서 <span class="codeph"> catalog_id</span>은(는) 경로의 첫 번째 토큰에 해당합니다. <span class="codeph"> image_id</span>은(는) 확장이 제거된 비디오의 이름입니다. 해당 ID의 이미지가 없는 경우 포스터 이미지가 표시되지 않습니다. </p> <p>기본 포스터 이미지가 표시되지 않도록 하려면 <span class="codeph"> none</span>을(를) 포스터 이미지 값으로 지정하십시오. <span class="codeph"><span class="varname"> isCommands</span></span>만 지정된 경우 이미지가 표시되기 전에 명령이 기본 포스터 이미지에 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

없음.

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
