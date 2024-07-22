---
description: eCatalog 뷰어에 대한 구성 속성 설명서.
solution: Experience Manager
title: 명령 참조 - 구성 속성
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

eCatalog 뷰어에 대한 구성 속성 설명서.

모든 구성 명령은 URL에서 설정하거나 `setParam()` 또는 `setParams()` 또는 두 가지 API 메서드를 모두 사용하여 설정할 수 있습니다. 서버측 구성 레코드에 지정된 모든 구성 속성을 지정할 수도 있습니다.

일부 구성 명령의 경우 해당 Viewer SDK 구성 요소의 클래스 이름 또는 인스턴스 이름으로 접두사를 추가할 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며 `setContainerId()` API 메서드에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 다릅니다. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어 `zoomstep` 명령은 다음과 같이 문서화되어 있습니다.

`[PageView.|<containerId>_pageView].zoomstep`

즉, 이 명령을 다음과 같이 사용할 수 있습니다.

* `zoomstep`(짧은 구문)
* `PageView.zoomstep`(구성 요소 클래스 이름으로 한정됨)
* `cont_pageView.zoomstep`(`cont`이(가) 컨테이너 요소의 ID라고 가정할 때 구성 요소 ID로 한정됨)

[모든 뷰어에 대해 공통되는 명령 참조 - 구성 특성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)도 참조하십시오.
