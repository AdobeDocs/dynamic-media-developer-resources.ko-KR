---
title: 명령 참조 - 구성 속성
description: 파노라마 뷰어에 대한 구성 속성 설명서.
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2: id: beaff0dd-a904-4c6b-8290-b527cd877d75id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

파노라마 뷰어에 대한 구성 속성 설명서.

모든 구성 명령은 URL에서 설정하거나 `setParam()` 및/또는 `setParams()` API 메서드를 사용하여 설정할 수 있습니다. 모든 구성 특성은 서버측 구성 레코드에도 지정할 수 있습니다.

일부 구성 명령에는 해당 HTML5 SDK 구성 요소의 클래스 이름 또는 인스턴스 이름이 접두사로 추가될 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며 `setContainerId()` API 메서드에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 다릅니다. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어 `vrrender` 명령은 다음과 같이 문서화되어 있습니다.

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

즉, 이 명령은 다음과 같은 방식으로 사용됩니다.

* `vrrender`(짧은 구문)
* `PanoramicView.vrrender`(구성 요소 클래스 이름으로 한정됨)
* `cont_panoramicView.vrrender`(컨테이너 요소의 ID가 cont라고 가정하고 구성 요소 ID로 한정됨)


[모든 뷰어에 대해 공통되는 명령 참조 - 구성 특성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)을 참조하십시오.

모든 뷰어에 대해 공통되는 [명령 참조 - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) 참조
