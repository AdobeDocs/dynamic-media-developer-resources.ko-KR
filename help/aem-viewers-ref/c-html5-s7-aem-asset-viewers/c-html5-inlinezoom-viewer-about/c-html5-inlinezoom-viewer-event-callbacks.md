---
description: 이벤트 콜백
solution: Experience Manager
title: 이벤트 콜백
feature: Dynamic Media Classic,Viewers,SDK/API,인라인 확대/축소
role: Developer,User
exl-id: c54c54ae-f98f-4cd4-8c36-c7e2a9f3c6df
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# 이벤트 콜백{#event-callbacks}

뷰어는 웹 페이지에서 뷰어 초기화 프로세스 또는 런타임 동작을 추적하는 데 사용하는 JavaScript 이벤트 콜백을 지원합니다.

콜백 핸들러는 이벤트 이름 및 `handlers` 속성을 사용하여 뷰어 생성자의 `config` JSON 개체에 해당 핸들러 함수를 전달하여 할당됩니다. 또는 `setHandlers()` API 메서드를 사용할 수 있습니다.

지원되는 뷰어 이벤트는 다음과 같습니다.

* `initComplete` - 뷰어 초기화가 완료되고 모든 내부 구성 요소가 생성되면 트리거되므로  `getComponent()` API를 사용할 수 있습니다. 콜백 처리기에서 인수를 사용하지 않습니다.

* `trackEvent` - Adobe Analytics과 같은 이벤트 추적 시스템에서 처리할 수 있는 뷰어 내에서 이벤트가 발생할 때마다 트리거됩니다. 콜백 처리기는 다음 인수를 사용합니다.

   * `objID {String}` 현재 사용되지 않습니다.
   * `compClass {String}` 현재 사용되지 않습니다.
   * `instName {String}` 이벤트를 트리거한 뷰어 SDK 구성 요소의 인스턴스 이름입니다.
   * `timeStamp {Number}` 이벤트 타임스탬프.
   * `eventInfo {String}` 이벤트 페이로드.

[FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) 및 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692)도 참조하십시오.
