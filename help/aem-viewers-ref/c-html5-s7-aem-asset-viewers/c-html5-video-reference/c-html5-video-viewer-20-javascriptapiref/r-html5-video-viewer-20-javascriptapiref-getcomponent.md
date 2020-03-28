---
description: 비디오 뷰어용 JavaScript API 참조
seo-description: 비디오 뷰어용 JavaScript API 참조
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: a2b073ab-d8a7-43cc-9cc8-80dd05a386f0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getComponent{#getcomponent}

비디오 뷰어용 JavaScript API 참조

`getComponent(componentId)`

뷰어에서 사용하는 뷰어 SDK 구성 요소에 대한 참조를 반환합니다. 웹 페이지에서는 이 방법을 사용하여 기본 뷰어의 동작을 확장하거나 사용자 지정할 수 있습니다. 뷰어 콜백이 실행된 후에만 이 메서드를 호출하고, 그렇지 않으면 뷰어 논리로 구성 요소를 아직 만들 수 없습니다. `initComplete`

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*` - 뷰어에서 `{String}` 사용하는 Viewer SDK 구성 요소의 ID입니다. 이 뷰어는 다음 구성 요소 ID를 지원합니다.

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
   <td colname="col1"> <p> <span class="codeph"> videoPlayer </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoPlayer </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> closedCaptionButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ClosedCaptionButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 제어 </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> emailShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.EmailShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> embedShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.EmbedShare </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK API를 사용하는 경우 Viewer SDK 네임스페이스에 [설명된 대로 올바른 정규화된 SDK 네임스페이스를 사용해야](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153)합니다.

특정 구성 요소에 대한 자세한 내용은 Viewer SDK API 설명서를 참조하십시오.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 SDK 구성 요소에 대한 참조입니다. 메서드가 지원되는 뷰어 구성 요소가 `null` `componentId` 아니거나 뷰어 논리로 구성 요소를 아직 만들지 않은 경우 반환됩니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
} 
})
```

