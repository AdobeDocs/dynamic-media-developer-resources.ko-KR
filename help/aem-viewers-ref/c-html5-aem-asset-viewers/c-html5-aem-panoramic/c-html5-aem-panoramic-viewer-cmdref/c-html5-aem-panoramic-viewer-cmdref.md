---
title: 명령 참조 - 구성 속성
description: 파노라마 뷰어에 대한 구성 속성 설명서입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

파노라마 뷰어에 대한 구성 속성 설명서입니다.

모든 구성 명령은 URL에서 설정하거나 `setParam()` 및/또는 `setParams()` API 메서드. 모든 구성 속성은 서버측 구성 레코드에서도 지정할 수 있습니다.

일부 구성 명령에는 해당 HTML5 SDK 구성 요소의 클래스 이름 또는 인스턴스 이름이 접두사로 붙을 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며, 에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 달라집니다 `setContainerId()` API 메서드. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함됩니다. 예, `vrrender` 명령은 다음과 같이 설명되어 있습니다.

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

즉, 이 명령은 다음과 같은 방식으로 사용됩니다.

* `vrrender` (짧은 구문)
* `PanoramicView.vrrender` (구성 요소 클래스 이름으로 한정됨)
* `cont_panoramicView.vrrender` (구성 요소 ID가 있는 자격이 있는 경우, cont가 컨테이너 요소의 ID라고 가정)


자세한 내용은 [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

자세한 내용은 [모든 뷰어에 공통되는 명령 참조 - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
