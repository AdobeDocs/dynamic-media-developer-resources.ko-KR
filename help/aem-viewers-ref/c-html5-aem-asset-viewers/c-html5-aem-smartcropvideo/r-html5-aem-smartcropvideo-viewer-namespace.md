---
title: 뷰어 SDK 네임스페이스
description: 뷰어 SDK 네임스페이스
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6cbf7eef-0d17-4411-9a74-22455009f66d
TQID: 'https://experienceleague.adobe.com/jP-ctDVghPscHD19iQPa4s5GnTyXKIIFOFu4UJTFo98'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%
---
# 뷰어 SDK 네임스페이스{#viewer-sdk-namespace}

뷰어는 많은 Viewer SDK 구성 요소로 구성됩니다. 일반적으로 웹 페이지는 SDK 구성 요소 API와 직접 상호 작용할 필요가 없으며 모든 일반적인 요구 사항은 뷰어 API 자체에서 다룹니다.

그러나 일부 고급 사용 사례에서는 웹 페이지가 `getComponent()` 뷰어 API를 사용하여 내부 SDK 구성 요소를 참조한 다음 SDK 자체의 모든 API를 유연하게 사용해야 합니다.

뷰어에서 SDK 구성 요소를 로드하고 초기화하는 데 사용되는 네임스페이스는 뷰어가 작동하는 환경에 따라 다릅니다. 뷰어가 Adobe Experience Manager에서 실행 중인 경우 뷰어는 SDK 구성 요소를 `s7viewers.s7sdk` 네임스페이스로 로드합니다. 마찬가지로 Dynamic Media Classic에서 제공하는 뷰어가 SDK을 `s7classic.s7sdk`에 로드합니다.

두 경우 모두 뷰어 내의 SDK에서 사용하는 네임스페이스에 접두사로 `s7viewers` 또는 `s7classic`이(가) 있습니다. 또한 SDK 사용 안내서 또는 SDK API 설명서에 사용되는 일반 `s7sdk` 네임스페이스와 다릅니다. 따라서 내부 뷰어 구성 요소와 통신하는 사용자 지정 애플리케이션 코드를 작성할 때 정규화된 SDK 네임스페이스를 사용하는 것이 중요합니다.

예를 들어, `StatusEvent.NOTF_VIEW_READY` 이벤트를 수신하려고 하며 뷰어가 Experience Manager에서 제공되는 경우 정규화된 이벤트 유형은 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`이며 이벤트 리스너 코드는 다음과 비슷합니다.

```javascript {.line-numbers}
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
