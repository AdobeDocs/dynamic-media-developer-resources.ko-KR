---
description: 이벤트 콜백
solution: Experience Manager
title: 이벤트 콜백
uuid: 325a3ccf-bae9-46f6-b3d0-70041a9548bb
feature: Dynamic Media Classic,뷰어,SDK/API,확대/축소
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# 이벤트 콜백{#event-callbacks}

뷰어는 웹 페이지가 뷰어 초기화 프로세스 또는 런타임 동작을 추적하는 데 사용하는 JavaScript 이벤트 콜백을 지원합니다.

콜백 핸들러는 이벤트 이름 및 `handlers` 속성을 가진 해당 핸들러 함수를 뷰어의 생성자에서 `config` JSON 개체에 전달하여 할당됩니다. 또는 `setHandlers()` API 메서드를 사용할 수 있습니다.

지원되는 뷰어 이벤트는 다음과 같습니다.

* `initComplete` - 뷰어 초기화가 완료되고 모든 내부 구성 요소가 생성될 때 트리거되므로  `getComponent()` API를 사용할 수 있습니다. 콜백 핸들러는 인수를 사용하지 않습니다.

* `trackEvent` - Adobe Analytics과 같은 이벤트 추적 시스템에서 처리할 수 있는 뷰어 내에서 이벤트가 발생할 때마다 트리거합니다. 콜백 핸들러는 다음 인수를 사용합니다.

   * `objID {String}` 현재 사용되지 않음.
   * `compClass {String}` 현재 사용되지 않음.
   * `instName {String}` 이벤트를 트리거한 Viewer SDK 구성 요소의 인스턴스 이름입니다.
   * `timeStamp {Number}` 이벤트 타임스탬프.
   * `eventInfo {String}` 이벤트 페이로드.

[ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) 및 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)도 참조하십시오.
