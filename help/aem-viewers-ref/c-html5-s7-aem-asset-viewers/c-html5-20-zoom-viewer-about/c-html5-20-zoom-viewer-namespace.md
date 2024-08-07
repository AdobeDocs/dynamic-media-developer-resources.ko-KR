---
title: Viewer SDK 네임스페이스
description: Viewer SDK 네임스페이스
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ad68dd09-d8df-4fc8-952a-ef82d9662de9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Viewer SDK 네임스페이스{#viewer-sdk-namespace}

이 뷰어는 많은 Viewer SDK 구성 요소로 구성됩니다. 일반적으로 웹 페이지는 SDK 구성 요소 API와 직접 상호 작용할 필요가 없으며 모든 일반적인 요구 사항은 뷰어 API 자체에서 다룹니다.

그러나 일부 고급 사용 사례에서는 웹 페이지가 `getComponent()` 뷰어 API를 사용하여 내부 SDK 구성 요소를 참조한 다음 SDK 자체의 모든 API를 유연하게 사용해야 합니다.

뷰어에서 SDK 구성 요소를 로드하고 초기화하는 데 사용되는 네임스페이스는 뷰어가 작동하는 환경에 따라 다릅니다. 뷰어가 Adobe Experience Manager에서 실행 중인 경우 뷰어는 SDK 구성 요소를 `s7viewers.s7sdk` 네임스페이스로 로드합니다. 마찬가지로 Dynamic Media Classic에서 제공하는 뷰어가 SDK를 `s7classic.s7sdk`에 로드합니다.

두 경우 모두 뷰어 내에서 SDK가 사용하는 네임스페이스에 `s7viewers` 또는 `s7classic`이(가) 접두사로 사용됩니다. 또한 SDK 사용 설명서나 SDK API 설명서에 사용된 일반 `s7sdk` 네임스페이스와 다릅니다. 따라서 내부 뷰어 구성 요소와 통신하는 사용자 지정 애플리케이션 코드를 작성할 때 정규화된 SDK 네임스페이스를 사용하는 것이 중요합니다.

예를 들어, `StatusEvent.NOTF_VIEW_READY` 이벤트를 수신하려고 하며 뷰어가 Experience Manager에서 제공되는 경우 정규화된 이벤트 유형은 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`이며 이벤트 리스너 코드는 다음과 비슷합니다.

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
