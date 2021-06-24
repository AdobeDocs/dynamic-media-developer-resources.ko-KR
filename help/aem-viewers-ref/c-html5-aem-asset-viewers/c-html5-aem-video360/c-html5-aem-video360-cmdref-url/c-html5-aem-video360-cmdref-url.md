---
description: Video360 뷰어에 대한 명령 참조 설명서입니다.
solution: Experience Manager
title: 명령 참조 - URL
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR 비디오
role: Developer,Business Practitioner
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 명령 참조 - URL{#command-reference-url}

Video360 뷰어에 대한 명령 참조 설명서입니다.

URL에서 모든 구성 명령을 설정할 수 있습니다. 또는 API 메서드 `setParam()` 또는 `setParams()` 를 사용하거나 둘 다 사용하여 구성 명령을 설정할 수 있습니다. 서버측 구성 레코드에 구성 속성을 지정할 수도 있습니다.

일부 구성 명령에는 해당 HTML5 뷰어 SDK 구성 요소의 인스턴스 이름 또는 클래스 이름을 접두사로 추가할 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며 `setContainerId()` API 메서드에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 다릅니다. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어 `playback`은 다음과 같이 설명되어 있습니다.

```
[Video360Player.|<containerId>_video360Player].playback
```

즉, 이 명령은 다음과 같은 방식으로 사용됩니다.

* `playback` (짧은 구문)
* `Video360Player.playback` (구성 요소 클래스 이름으로 한정됨)
* `cont_video360Player.playback` (컨테이너 요소의 ID라고 가정하 `cont` 는 경우 구성 요소 ID가 검증됨)

모든 뷰어에 공통되는 [명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)를 참조하십시오.
