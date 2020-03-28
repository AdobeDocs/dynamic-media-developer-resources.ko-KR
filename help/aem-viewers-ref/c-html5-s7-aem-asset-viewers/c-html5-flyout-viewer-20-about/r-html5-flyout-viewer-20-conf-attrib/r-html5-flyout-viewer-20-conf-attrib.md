---
description: 플라이아웃 뷰어에 대한 구성 속성 설명서
seo-description: 플라이아웃 뷰어에 대한 구성 속성 설명서
seo-title: 명령 참조 - 구성 속성
solution: Experience Manager
title: 명령 참조 - 구성 속성
topic: Dynamic media
uuid: d7e89a24-a235-4f20-86d1-25aacd118880
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

플라이아웃 뷰어에 대한 구성 속성 설명서

URL에서 모든 구성 명령을 설정할 수 있습니다. 또는 API 메서드를 `setParam()`사용하거나 `setParams()`둘 다 사용할 수 있습니다. 서버측 구성 레코드에 모든 구성 속성을 지정할 수도 있습니다.

일부 구성 명령에는 해당 Viewer SDK 구성 요소의 클래스 이름 또는 인스턴스 이름이 접두사로 붙습니다. 구성 요소의 인스턴스 이름은 동적이며 API 메서드에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 `setContainerId()` 달라집니다. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어 이 `zoomfactor` 명령은 다음과 같이 문서화됩니다.

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

이 명령은 다음과 같이 사용됩니다.

* `zoomfactor` (짧은 구문)
* `FlyoutZoomView.zoomfactor` (구성 요소 클래스 이름으로 적격)
* `cont_flyout.zoomfactor` (컨테이너 요소의 ID라고 가정하고 구성 요소 ID로 `cont` 적음)

모든 [뷰어에 공통으로 사용되는 명령 참조 - 구성 특성 참조](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
