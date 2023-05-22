---
title: 명령 참조 - 구성 속성
description: 플라이아웃 뷰어에 대한 구성 속성 설명서
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

플라이아웃 뷰어에 대한 구성 속성 설명서

URL에서 모든 구성 명령을 설정할 수 있습니다. 또는 다음을 사용할 수 있습니다 `setParam()`, `setParams()`또는 두 API 메서드 모두 서버측 구성 레코드에 구성 속성을 지정할 수도 있습니다.

일부 구성 명령에는 해당 Viewer SDK 구성 요소의 클래스 이름 또는 인스턴스 이름이 접두사로 추가됩니다. 구성 요소의 인스턴스 이름은 동적이며,에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 다릅니다. `setContainerId()` API 메서드. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어 `zoomfactor` 명령은 다음과 같이 문서화되어 있습니다.

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

명령은 다음과 같이 사용됩니다.

* `zoomfactor` (짧은 구문)
* `FlyoutZoomView.zoomfactor` (구성 요소 클래스 이름으로 한정됨)
* `cont_flyout.zoomfactor` (구성 요소 ID로 자격이 부여됩니다. `cont` 는 컨테이너 요소의 ID입니다)

참조: [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
