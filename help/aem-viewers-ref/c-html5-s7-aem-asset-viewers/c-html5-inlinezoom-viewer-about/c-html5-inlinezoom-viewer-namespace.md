---
title: Viewer SDK 네임스페이스
description: Viewer SDK 네임스페이스
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b61a17-f9ae-4e71-bd78-276674193044
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Viewer SDK 네임스페이스{#viewer-sdk-namespace}

뷰어는 많은 Viewer SDK 구성 요소로 구성됩니다. 일반적으로 웹 페이지는 SDK 구성 요소 API와 직접 상호 작용할 필요가 없습니다. 모든 일반적인 요구 사항은 뷰어 API 자체에서 다룹니다.

그러나 일부 고급 사용 사례에서는 웹 페이지에서 `getComponent()` 뷰어 API 와 SDK 자체의 모든 API를 사용합니다.

뷰어가 SDK 구성 요소를 로드하고 초기화하는 데 사용되는 네임스페이스는 뷰어가 작동하는 환경에 따라 다릅니다. 뷰어가 Adobe Experience Manager에서 실행 중인 경우 뷰어는 SDK 구성 요소를 `s7viewers.s7sdk` 네임스페이스. 마찬가지로 Dynamic Media Classic에서 제공되는 뷰어는 SDK를 `s7classic.s7sdk`.

어느 경우든 뷰어 내에서 SDK에서 사용하는 네임스페이스에는 다음 중 하나가 있습니다 `s7viewers` 또는 `s7classic` 를 접두사로 추가합니다. 그리고 평지와 다르죠 `s7sdk` sdk 사용 안내서 또는 SDK API 설명서에 사용되는 네임스페이스입니다.

이러한 이유로 내부 뷰어 구성 요소와 통신하는 사용자 지정 애플리케이션 코드를 작성할 때 정규화된 SDK 네임스페이스를 사용하는 것이 중요합니다.

예를 들어, `StatusEvent.NOTF_VIEW_READY` 이벤트 및 뷰어가 Experience Manager에서 제공되는 경우, 정규화된 이벤트 유형은 다음과 같습니다. `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`및 이벤트 리스너 코드는 다음과 유사합니다.

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
