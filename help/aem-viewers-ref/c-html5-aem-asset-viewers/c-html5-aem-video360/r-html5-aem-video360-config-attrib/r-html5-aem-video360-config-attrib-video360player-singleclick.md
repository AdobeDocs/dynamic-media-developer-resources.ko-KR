---
description: Video360 뷰어에 대한 구성 속성입니다.
seo-description: Video360 뷰어에 대한 구성 속성입니다.
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
feature: Dynamic Media Classic,뷰어,SDK/API,360 VR 비디오
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 11%

---


# Video360Player.singleclick{#video-player-singleclick}

Video360 뷰어에 대한 구성 속성입니다.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 중지를 전환하도록 한 번의 클릭/탭 매핑을 구성합니다. <span class="codeph"> none</span>으로 설정하면 재생/일시 정지하기 위해 한 번의 클릭/탭을 사용할 수 없습니다. <span class="codeph"> playPause</span>로 설정된 경우 비디오를 클릭하면 비디오 재생과 일시 중지 간에 전환됩니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이 경우 <span class="codeph"> singlick</span> 비헤이비어가 비활성화됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

