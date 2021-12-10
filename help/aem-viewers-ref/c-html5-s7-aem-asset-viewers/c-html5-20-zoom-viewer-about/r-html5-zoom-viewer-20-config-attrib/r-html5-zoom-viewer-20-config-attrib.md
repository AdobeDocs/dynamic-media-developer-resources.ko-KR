---
title: 명령 참조 - 구성 속성
description: 확대/축소 뷰어에 대한 구성 속성 설명서입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

확대/축소 뷰어에 대한 구성 속성 설명서입니다.

모든 구성 명령은 URL에서 설정하거나 `setParam()`, 또는 `setParams()`또는 둘 다, API 메서드. 모든 구성 속성은 서버측 구성 레코드에서도 지정할 수 있습니다.

일부 구성 명령에는 해당 Viewer SDK 구성 요소의 클래스 이름 또는 인스턴스 이름이 접두사로 붙을 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며, 에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 달라집니다 `setContainerId()` API 메서드. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예, `zoomstep` 명령은 다음과 같이 설명되어 있습니다.

`[ZoomView.|<containerId>_zoomView].zoomstep`

즉, 명령을

* `zoomstep` (짧은 구문)
* `ZoomView.zoomstep` (구성 요소 클래스 이름으로 한정됨)
* `cont_zoomView.zoomstep` (구성 요소 ID가 있는 경우 검증됨, `cont` 는 컨테이너 요소의 ID입니다.

참조 - [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
