---
title: 명령 참조 - 구성 속성
description: eCatalog 뷰어에 대한 구성 속성 설명서입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

eCatalog 뷰어에 대한 구성 속성 설명서입니다.

모든 구성 명령은 URL에서 설정하거나 `setParam()`, 또는 `setParams()`또는 둘 다, API 메서드. 서버측 구성 레코드에 지정된 구성 속성을 지정할 수도 있습니다.

일부 구성 명령의 경우 해당 Viewer SDK 구성 요소의 클래스 이름 또는 인스턴스 이름을 접두사로 추가할 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며, 에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 달라집니다 `setContainerId()` API 메서드. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예, `zoomstep` 명령은 다음과 같이 설명되어 있습니다.

`[PageView.|<containerId>_pageView].zoomstep`

즉, 이 명령을

* `zoomstep` (짧은 구문)
* `PageView.zoomstep` (구성 요소 클래스 이름으로 한정됨)
* `cont_pageView.zoomstep` (구성 요소 ID가 있는 경우 검증됨, `cont` 는 컨테이너 요소의 ID입니다.

참조 - [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
