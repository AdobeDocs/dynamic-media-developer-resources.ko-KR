---
description: 널
seo-description: 널
seo-title: 뷰어 SDK 네임스페이스
solution: Experience Manager
title: 뷰어 SDK 네임스페이스
topic: Dynamic media
uuid: e0113556-708c-4898-93f9-b3888de00afc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 뷰어 SDK 네임스페이스{#viewer-sdk-namespace}

뷰어는 많은 Viewer SDK 구성 요소로 구성됩니다. 대부분의 경우 웹 페이지는 SDK 구성 요소 API와 직접 상호 작용할 필요가 없습니다.모든 일반적인 요구 사항은 뷰어 API 자체에서 다룹니다.

그러나 일부 고급 사용 사례에서는 웹 페이지에서 뷰어 API를 사용하여 내부 SDK 구성 요소에 대한 참조를 얻은 다음 SDK 자체의 모든 유연한 API를 사용해야 `getComponent()` 합니다.

뷰어에서 SDK 구성 요소를 로드하고 초기화하는 데 사용되는 네임스페이스는 뷰어가 작동 중인 환경에 따라 다릅니다. 뷰어가 AEM(Adobe Experience Manager)에서 실행 중인 경우 뷰어는 SDK 구성 요소를 `s7viewers.s7sdk` 네임스페이스로 로드합니다. 마찬가지로 Scene7 Publishing System에서 제공되는 뷰어는 SDK를 에 로드합니다 `s7classic.s7sdk`.

두 경우 모두 뷰어 내에서 SDK가 사용하는 네임스페이스에 `s7viewers` 또는 `s7classic` 접두사가 있습니다. 또한 SDK 사용 안내서 또는 SDK API 설명서에 사용되는 일반 `s7sdk` 네임스페이스와 다릅니다.

따라서 내부 뷰어 구성 요소와 통신하는 사용자 정의 응용 프로그램 코드를 작성할 때 정규화된 SDK 네임스페이스를 사용해야 합니다.

예를 들어, 이벤트를 수신하려고 하고 뷰어가 AEM에서 제공되는 경우, 정규화된 이벤트 유형이 `StatusEvent.NOTF_VIEW_READY` `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`되고 이벤트 리스너 코드는 다음과 유사해 보입니다.

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

