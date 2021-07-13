---
description: Video360 Viewer에 대한 구성 속성 설명서입니다.
solution: Experience Manager
title: 명령 참조 - 구성 속성
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR 비디오
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

Video360 Viewer에 대한 구성 속성 설명서입니다.

모든 구성 명령은 URL이나 `setParam()`, `setParams()` 또는 두 가지 모두 API 메서드를 사용하여 설정할 수 있습니다. 모든 구성 속성은 서버측 구성 레코드에서도 지정할 수 있습니다.

일부 구성 명령에는 해당 Viewer SDK 구성 요소의 클래스 이름 또는 인스턴스 이름이 접두사로 붙을 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며 `setContainerId()` API 메서드에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 다릅니다. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어 `playback` 명령은 다음과 같이 설명되어 있습니다.

`[VideoPlayer.|<containerId>_videoPlayer].playback`

즉, 이 명령을 다음과 같이 사용할 수 있습니다.

* `playback` (짧은 구문)
* `VideoPlayer.playback` (구성 요소 클래스 이름으로 한정됨)
* `cont_videoPlayer.playback` (컨테이너 요소의 ID라고 가정하 `cont` 는 경우 구성 요소 ID가 검증됨)

모든 뷰어에 공통되는 [명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)을 참조하십시오.
