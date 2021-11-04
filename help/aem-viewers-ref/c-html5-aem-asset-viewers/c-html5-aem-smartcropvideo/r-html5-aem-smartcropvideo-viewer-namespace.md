---
title: Viewer SDK 네임스페이스
description: Viewer SDK 네임스페이스
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Viewer SDK 네임스페이스{#viewer-sdk-namespace}

The viewer is built of many Viewer SDK components. 일반적으로 웹 페이지는 SDK 구성 요소 API와 직접 상호 작용할 필요가 없습니다. 모든 일반적인 요구 사항은 뷰어 API 자체에서 다룹니다.

그러나 일부 고급 사용 사례에서는 웹 페이지에서 `getComponent()` 뷰어 API 와 SDK 자체의 모든 API를 사용합니다.

뷰어가 SDK 구성 요소를 로드하고 초기화하는 데 사용되는 네임스페이스는 뷰어가 작동하는 환경에 따라 다릅니다. 뷰어가 Adobe Experience Manager에서 실행 중인 경우 뷰어는 SDK 구성 요소를 `s7viewers.s7sdk` 네임스페이스. 마찬가지로 Dynamic Media Classic에서 제공되는 뷰어는 SDK를 `s7classic.s7sdk`.

어느 경우든 뷰어 내에서 SDK에서 사용하는 네임스페이스에는 다음 중 하나가 있습니다 `s7viewers` 또는 `s7classic` 를 접두사로 추가합니다. And, it is different from the plain `s7sdk` namespace used in the SDK User Guide or SDK API documentation. 이러한 이유로 내부 뷰어 구성 요소와 통신하는 사용자 지정 애플리케이션 코드를 작성할 때 정규화된 SDK 네임스페이스를 사용하는 것이 중요합니다.

For example, if you plan to listen to `StatusEvent.NOTF_VIEW_READY` event and the viewer is served from Experience Manager, the fully qualified event type is `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`, and the event listener code looks similar to the following:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
