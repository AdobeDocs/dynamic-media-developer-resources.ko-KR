---
title: 명령 참조 - URL
description: 스마트 자르기 비디오 뷰어에 대한 명령 참조 설명서입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d0797c10-2379-45f7-9e8d-a5eb56638db8
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# 명령 참조 - URL{#command-reference-url}

스마트 자르기 비디오 뷰어에 대한 명령 참조 설명서입니다.

URL에서 모든 구성 명령을 설정할 수 있습니다. 또는 API 메서드를 사용할 수 있습니다 `setParam()`, 또는 `setParams()`또는 두 가지 모두를 사용하여 구성 명령을 설정할 수 있습니다. 서버측 구성 레코드에 구성 속성을 지정할 수도 있습니다.

일부 구성 명령에 해당 Viewer SDK 구성 요소의 클래스 이름 또는 인스턴스 이름을 접두사로 추가할 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며,에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 다릅니다. `setContainerId()` API 메서드. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어, `playback` 는 다음과 같이 문서화되어 있습니다.

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

즉, 이 명령은 다음과 같은 방식으로 사용됩니다.

* `playback` (짧은 구문)
* `SmartCropVideoPlayer.playback` (구성 요소 클래스 이름으로 한정됨)
* `cont_smartCropVideoPlayer.playback` (다음을 가정하고 구성 요소 ID로 자격이 부여됨) `cont` 는 컨테이너 요소의 ID입니다)

참조: [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

참조: [모든 뷰어에 대해 공통되는 명령 참조 - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
