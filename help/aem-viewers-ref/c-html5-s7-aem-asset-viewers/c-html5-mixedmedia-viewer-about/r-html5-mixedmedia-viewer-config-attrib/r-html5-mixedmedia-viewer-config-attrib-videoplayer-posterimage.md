---
description: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic Media
uuid: 28663f44-11cb-4522-bd12-d6bec17b4173
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 재생되기 전에 첫 번째 프레임에 표시할 이미지입니다. <span class="codeph"> serverurl</span>에 대해 해결되었습니다. URL에 지정된 경우 다음을 HTTP로 인코딩합니다. </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> </span> %26 <span class="codeph"> 으로(&amp;A)</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> = </span> %3D <span class="codeph"> 로</span> </p> </li> 
     </ul> </p> <p><span class="codeph"><span class="varname"> image_id</span></span> 값이 생략되면 구성 요소는 해당 자산에 대한 기본 포스터 이미지를 대신 사용하려고 합니다. </p> <p>비디오가 경로로 지정되면 기본 포스터 이미지 카탈로그 ID는 <span class="codeph"> catalog_id/image_id</span> 쌍에서 추출됩니다. 여기서 <span class="codeph"> catalog_id</span>는 경로의 첫 번째 토큰에 해당하고 <span class="codeph"> image_id</span>는 확장명이 제거된 비디오의 이름입니다. 해당 ID를 가진 이미지가 없는 경우 포스터 이미지가 표시되지 않습니다. </p> <p>기본 포스터 이미지가 표시되지 않도록 하려면 포스터 이미지 값으로 <span class="codeph"> none</span>을 지정합니다. <span class="codeph"><span class="varname"> isCommands</span></span>만 지정된 경우 이미지가 표시되기 전에 기본 포스터 이미지에 명령이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

없음.

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
