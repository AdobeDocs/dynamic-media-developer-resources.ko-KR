---
description: eCatalog 뷰어에 대한 구성 특성 설명서입니다.
seo-description: eCatalog 뷰어에 대한 구성 특성 설명서입니다.
seo-title: 명령 참조 - 구성 속성
solution: Experience Manager
title: 명령 참조 - 구성 속성
topic: Dynamic media
uuid: 823ad411-653a-44de-97de-147e3b27a917
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

eCatalog 뷰어에 대한 구성 특성 설명서입니다.

모든 구성 명령은 URL에서 설정하거나 API 메서드를 `setParam()`사용하거나 `setParams()`둘 다 사용할 수 있습니다. 서버측 구성 레코드에 지정된 구성 속성을 지정할 수도 있습니다.

일부 구성 명령의 경우 해당 Viewer SDK 구성 요소의 클래스 이름 또는 인스턴스 이름으로 접두사를 지정할 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며 API 메서드에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 `setContainerId()` 달라집니다. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어 `zoomstep` 명령은 다음과 같이 문서화됩니다.

`[PageView.|<containerId>_pageView].zoomstep`

즉, 이 명령을 다음과 같이 사용할 수 있습니다.

* `zoomstep` (짧은 구문)
* `PageView.zoomstep` (구성 요소 클래스 이름으로 적격)
* `cont_pageView.zoomstep` (구성 요소 ID로 적음, 컨테이너 요소의 ID `cont` 라고 가정하는 경우)

모든 [뷰어에 공통으로 사용되는 명령 참조 - 구성 특성 참조](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
