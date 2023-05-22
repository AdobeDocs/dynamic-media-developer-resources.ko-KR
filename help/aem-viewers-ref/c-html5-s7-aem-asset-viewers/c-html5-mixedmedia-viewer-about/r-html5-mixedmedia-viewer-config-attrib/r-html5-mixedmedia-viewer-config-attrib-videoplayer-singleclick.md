---
title: VideoPlayer.singleclick
description: VideoPlayer.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2ec6d871-05d9-4d85-b031-e64386f5d2e9
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`없음|playPause`*`

<table id="table_53A26E1617CB411B9586203CB9AA1AB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 없음|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 중지를 전환하기 위한 한 번의 클릭/누르기 매핑을 구성합니다. 을 로 설정 <span class="codeph"> 없음</span> 한 번 클릭/탭하여 재생/일시 중지를 비활성화합니다. 로 설정된 경우 <span class="codeph"> playPause</span>를 클릭하면 비디오 재생과 일시 중지 간을 전환합니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이런 경우, <span class="codeph"> singleclick</span> 비헤이비어가 비활성화되었습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`playPause`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=none`
