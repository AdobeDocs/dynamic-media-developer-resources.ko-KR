---
title: 이벤트 콜백
description: 이벤트 콜백
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c54c54ae-f98f-4cd4-8c36-c7e2a9f3c6df
source-git-commit: f970421ccc482b698343aa18e7dfde7bea4c2a89
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# 이벤트 콜백{#event-callbacks}

뷰어는 웹 페이지가 뷰어 초기화 프로세스 또는 런타임 동작을 추적하는 데 사용하는 JavaScript 이벤트 콜백을 지원합니다.

`handlers` 속성이 있는 이벤트 이름 및 해당 처리기 함수를 뷰어의 생성자에 있는 `config` JSON 개체로 전달하여 콜백 처리기를 할당합니다. 또는 `setHandlers()` API 메서드를 사용할 수 있습니다.

지원되는 뷰어 이벤트는 다음과 같습니다.

* `initComplete` - 뷰어 초기화가 완료되고 모든 내부 구성 요소가 만들어지면 트리거되므로 `getComponent()` API를 사용할 수 있습니다. 콜백 핸들러는 인수를 사용하지 않습니다.

* `trackEvent` - Adobe Analytics과 같은 이벤트 추적 시스템에서 처리할 수 있는 뷰어 내에서 이벤트가 발생할 때마다 트리거됩니다. 콜백 핸들러는 다음 인수를 사용합니다.

   * `objID {String}`은(는) 현재 사용되지 않습니다.
   * `compClass {String}`은(는) 현재 사용되지 않습니다.
   * `instName {String}` 이벤트를 트리거한 Viewer SDK 구성 요소의 인스턴스 이름입니다.
   * `timeStamp {Number}` 이벤트 타임스탬프.
   * `eventInfo {String}` 이벤트 페이로드.

[FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) 및 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692)도 참조하세요.
