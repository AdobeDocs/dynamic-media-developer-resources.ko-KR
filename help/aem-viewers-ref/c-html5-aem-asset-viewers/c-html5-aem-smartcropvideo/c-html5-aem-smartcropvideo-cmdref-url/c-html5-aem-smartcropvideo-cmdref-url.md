---
title: 명령 참조 - URL
description: 스마트 자르기 비디오 뷰어에 대한 명령 참조 설명서입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 1ed78e0d-9b93-4c66-b558-fac15c51e944
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# 명령 참조 - URL{#command-reference-url}

스마트 자르기 비디오 뷰어에 대한 명령 참조 설명서입니다.

URL에서 모든 구성 명령을 설정할 수 있습니다. 또는 API 메서드를 사용할 수 있습니다 `setParam()`, 또는 `setParams()`또는 둘 다 구성 명령을 설정합니다. 서버측 구성 레코드에 구성 속성을 지정할 수도 있습니다.

일부 구성 명령에는 클래스 이름이나 해당 Viewer SDK 구성 요소의 인스턴스 이름을 접두사로 추가할 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며, 에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 달라집니다 `setContainerId()` API 메서드. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예, `playback` 는 다음과 같이 설명되어 있습니다.

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

즉, 이 명령은 다음과 같은 방식으로 사용됩니다.

* `playback` (짧은 구문)
* `SmartCropVideoPlayer.playback` (구성 요소 클래스 이름으로 한정됨)
* `cont_smartCropVideoPlayer.playback` (구성 요소 ID가 있는 경우 `cont` 는 컨테이너 요소의 ID입니다.

참조 - [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

참조 - [모든 뷰어에 공통되는 명령 참조 - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
