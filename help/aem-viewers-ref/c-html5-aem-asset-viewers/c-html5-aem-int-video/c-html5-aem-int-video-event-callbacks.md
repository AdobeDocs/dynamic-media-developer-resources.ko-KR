---
description: 널
seo-description: 널
seo-title: 이벤트 콜백
solution: Experience Manager
title: 이벤트 콜백
topic: Dynamic media
uuid: b9252d4b-cff1-42eb-9e56-553091f854b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 이벤트 콜백{#event-callbacks}

뷰어는 웹 페이지에서 뷰어 초기화 프로세스 또는 런타임 동작을 추적하는 데 사용하는 JavaScript 이벤트 콜백을 지원합니다.

콜백 핸들러는 이벤트 이름 및 해당 핸들러 함수를 `handlers` 속성과 함께 뷰어 생성자의 JSON `config` 개체에 전달하여 할당됩니다. 또는 API 메서드를 사용할 수 `setHandlers()` 있습니다.

지원되는 뷰어 이벤트는 다음과 같습니다.

* `initComplete` - 뷰어 초기화가 완료되고 모든 내부 구성 요소가 생성될 때 트리거되므로 API를 사용할 수 `getComponent()` 있습니다. 콜백 핸들러는 인수를 사용하지 않습니다.
* `trackEvent` - Adobe Analytics와 같은 이벤트 추적 시스템에서 처리할 수 있는 뷰어 내에서 이벤트가 발생할 때마다 트리거합니다. 콜백 핸들러는 다음 인수를 사용합니다.

   * `objID {String}` 현재 사용되지 않습니다.
   * `compClass {String}` 현재 사용되지 않습니다.
   * `instName {String}` 이벤트를 트리거한 뷰어 SDK 구성 요소의 인스턴스 이름입니다.
   * `timeStamp {Number}` 이벤트 타임스탬프
   * `eventInfo {String}` 이벤트 페이로드.

* `quickViewActivate` - 사용자가 인터랙티브한 견본 구성 요소 또는 비디오 재생 끝에 표시된 &quot;클릭유도문안&quot; 화면에서 인터랙티브한 견본을 클릭하거나 탭할 때 트리거합니다. 콜백 핸들러는 다음 필드가 있는 JSON 개체인 유일한 인수를 사용합니다.

   * `sku` { `String`} 대화형 견본과 연결된 SKU 값.
   * `<additionalVariable>` 대화형 견본과 연결된 추가 변수가 { `String`} 0개 이상 있습니다.

InteractiveVideoViewer [및 setHandler](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) 를 [참조하십시오](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
