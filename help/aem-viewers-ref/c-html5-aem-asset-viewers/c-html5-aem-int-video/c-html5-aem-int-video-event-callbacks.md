---
title: 이벤트 콜백
description: 이벤트 콜백
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '210'
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

* `quickViewActivate` - 사용자가 대화형 견본 구성 요소 내에서 또는 비디오 재생 끝에 표시된 &quot;콜 투 액션&quot; 화면에서 대화형 견본을 클릭하거나 탭할 때 트리거됩니다. 콜백 핸들러는 다음 필드가 있는 JSON 개체인 유일한 인수를 사용합니다.

   * 대화형 견본과 연결된 `sku` { `String`} SKU 값입니다.
   * `<additionalVariable>` { `String`}개 이상의 추가 변수가 대화형 견본과 연결되어 있습니다.

[InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) 및 [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)도 참조하세요.
