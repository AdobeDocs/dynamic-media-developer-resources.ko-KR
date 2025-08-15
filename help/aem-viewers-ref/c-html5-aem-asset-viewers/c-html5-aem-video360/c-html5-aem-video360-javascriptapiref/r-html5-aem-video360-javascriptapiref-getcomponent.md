---
title: getComponent
description: Video360 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: bc5f0046-8e20-4ff0-a90f-05c38f686ad2
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# getComponent{#getcomponent}

Video360 뷰어에 대한 JavaScript API 참조.

`getComponent(componentId)`

뷰어에서 사용하는 뷰어 SDK 구성 요소에 대한 참조를 반환합니다. 웹 페이지는 이 메서드를 사용하여 기본 뷰어의 동작을 확장하거나 사용자 지정할 수 있습니다. `initComplete` 뷰어 콜백이 실행된 후에만 이 메서드를 호출하십시오. 그렇지 않으면 뷰어 논리에 의해 구성 요소가 아직 만들어지지 않았을 수 있습니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` 뷰어에서 사용하는 Viewer SDK 구성 요소의 ID입니다. 이 뷰어는 다음 구성 요소 ID를 지원합니다.

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>구성 요소 ID </p> </th> 
   <th colname="col2" class="entry"> <p>뷰어 SDK 구성 요소 클래스 이름 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컨테이너 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> video360Player </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.Video360Player </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mutableVolume </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> playPauseButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoScrubber </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoTime </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컨트롤 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> embedShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sk.share.EmbedShare </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK API를 사용하여 작업할 때는 [뷰어 SDK 네임스페이스](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621)에 설명된 대로 올바른 정규화된 SDK 네임스페이스를 사용해야 합니다.

특정 구성 요소에 대한 자세한 내용은 *HTML5 뷰어 SDK API* 설명서를 참조하십시오.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`은(는) Viewer SDK 구성 요소에 대한 참조입니다. `null`이(가) 지원되는 뷰어 구성 요소가 아니거나 구성 요소가 아직 뷰어 논리에 의해 만들어지지 않은 경우 메서드가 `componentId`을(를) 반환합니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var video360Player = <instance>.getComponent("video360Player"); 
} 
})
```
