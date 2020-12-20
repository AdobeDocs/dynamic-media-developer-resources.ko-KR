---
description: 확대/축소 뷰어에 대한 구성 속성 설명서입니다.
seo-description: 확대/축소 뷰어에 대한 구성 속성 설명서입니다.
seo-title: 명령 참조 - 구성 속성
solution: Experience Manager
title: 명령 참조 - 구성 속성
topic: Dynamic media
uuid: 1bcc879a-12ec-4924-ac05-2e4c1d6e4597
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# 명령 참조 - 구성 특성{#command-reference-configuration-attributes}

확대/축소 뷰어에 대한 구성 속성 설명서입니다.

모든 구성 명령은 URL로 설정하거나 `setParam()` 또는 `setParams()` 또는 두 API 메서드를 사용하여 설정할 수 있습니다. 구성 속성은 서버측 구성 레코드에도 지정할 수 있습니다.

일부 구성 명령에는 해당 뷰어 SDK 구성 요소의 클래스 이름 또는 인스턴스 이름이 접두사로 포함될 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며 `setContainerId()` API 메서드에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 달라집니다. 설명서에는 이러한 명령에 대한 선택적 접두어가 포함되어 있습니다. 예를 들어 `zoomstep` 명령은 다음과 같이 문서화됩니다.

`[ZoomView.|<containerId>_zoomView].zoomstep`

즉, 이 명령을 다음과 같이 사용할 수 있습니다.

* `zoomstep` (짧은 구문)
* `ZoomView.zoomstep` (구성 요소 클래스 이름으로 적격)
* `cont_zoomView.zoomstep` (컨테이너 요소의 ID라고 가정하 `cont` 는 구성 요소 ID로 적격)

모든 뷰어에 공통인 [명령 참조 - 구성 특성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 참조
