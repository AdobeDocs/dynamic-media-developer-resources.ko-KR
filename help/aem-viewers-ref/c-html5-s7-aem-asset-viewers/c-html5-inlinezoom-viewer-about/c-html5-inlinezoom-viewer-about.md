---
description: 인라인 확대/축소 뷰어는 이미지 뷰어입니다. 사용자가 기본 보기를 롤업하거나 터치하면 해당 정적 이미지 위에 확대/축소된 버전이 표시된 정적 이미지가 표시됩니다. 이 뷰어는 이미지 세트에서 작동하며 색상 견본을 사용하여 탐색합니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.
keywords: 응답형
solution: Experience Manager
title: 인라인 확대/축소
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '2385'
ht-degree: 0%

---

# 인라인 확대/축소{#inline-zoom}

인라인 확대/축소 뷰어는 이미지 뷰어입니다. 사용자가 기본 보기를 롤업하거나 터치하면 해당 정적 이미지 위에 확대/축소된 버전이 표시된 정적 이미지가 표시됩니다. 이 뷰어는 이미지 세트에서 작동하며 색상 견본을 사용하여 탐색합니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형은 504입니다.

[시스템 요구 사항 및 사전 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)을 참조하십시오.

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## 인라인 확대/축소 뷰어 사용 {#section-f21ac23d3f6449ad9765588d69584772}

인라인 확대/축소 뷰어는 런타임 시 뷰어가 다운로드한 기본 JavaScript 파일 및 도우미 파일 세트(단일 JavaScript에는 이 특정 뷰어에서 사용하는 모든 뷰어 SDK 구성 요소, 자산 및 CSS)에 포함됩니다.

인라인 확대/축소 뷰어는 이미지 제공 뷰어와 함께 제공되는 프로덕션 준비 HTML 페이지를 사용하는 팝업 모드에서 또는 문서화된 API를 사용하여 대상 웹 페이지에 통합되는 포함된 모드에서 모두 사용할 수 있습니다.

구성 및 스키닝은 다른 뷰어의 구성과 유사합니다. 사용자 지정 CSS를 사용하여 스키닝을 적용할 수 있습니다.

모든 뷰어에 공통되는 [명령 참조 - 구성 속성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)를 참조하십시오.

## 인라인 확대/축소 뷰어와 상호 작용 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

인라인 확대/축소 뷰어는 다른 모바일 애플리케이션에서 일반적으로 사용되는 단일 터치 및 다중 터치 제스처를 지원합니다.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>제스처 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>단일 탭 </p> </td> 
   <td colname="col2"> <p> 견본의 기본 및 보조 확대/축소 수준 간에 플라이아웃 보기 또는 변경 사항을 활성화하고 새 축소판을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>가로 밀기 또는 밀기 </p> </td> 
   <td colname="col2"> <p> 견본 막대의 색상 견본 목록을 스크롤합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세로 밀기 </p> </td> 
   <td colname="col2"> <p>제스처가 색상 견본 영역 내에서 수행되면 기본 페이지 스크롤이 수행됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

이 뷰어는 또한 터치 스크린과 마우스로 Windows 장치에서 터치 입력과 마우스 입력을 모두 지원합니다. 그러나 이 지원은 Chrome, Internet Explorer 11 및 Edge 웹 브라우저만 지원합니다.

이 뷰어는 키보드로 액세스할 수 있습니다.

[키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)을 참조하십시오.

## 인라인 확대/축소 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 동작에 대한 요구 사항이 다릅니다. 경우에 따라 웹 페이지에서 별도의 브라우저 창에서 뷰어를 여는 클릭 가능한 링크를 제공합니다. 다른 경우, 뷰어를 호스팅 페이지에 직접 포함해야 할 수도 있습니다. 후자의 경우, 웹 페이지에는 정적 페이지 레이아웃이 있거나, 서로 다른 장치 또는 서로 다른 브라우저 창 크기에 대해 다르게 표시되는 응답형 디자인을 사용할 수 있습니다. 이러한 요구 사항을 수용하기 위해 뷰어는 다음 세 가지 기본 작업 모드를 지원합니다. 팝업, 고정 크기 포함 및 응답형 포함

**팝업**

팝업 모드에서 뷰어는 별도의 웹 브라우저 창이나 탭에서 열립니다. 전체 브라우저 창 영역을 사용하고 브라우저 창의 크기가 조정되거나 장치 방향이 변경될 때 조정됩니다.

이 모드는 모바일 장치에 가장 일반적입니다. 웹 페이지는 `window.open()` JavaScript 호출을 사용하여 뷰어를 로드하거나, 올바르게 구성된 `A` HTML 요소 또는 기타 적절한 방법을 사용하여 로드합니다.

팝업 모드 `FlyoutViewer.html`에 기본 제공 HTML 페이지를 사용하는 것이 좋습니다. 표준 Image Serving-Viewers 배포의 [!DNL html5/] 하위 폴더 아래에 있습니다.

`<s7viewers_root>/html5/FlyoutViewer.html`

또한 인라인 확대/축소 모드에서 작동하도록 FlyoutZoomView 구성 요소를 구성해야 합니다. 인라인 확대/축소 뷰어에 기본 제공 `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` 사전 설정 또는 이 사전 설정에서 파생된 사용자 정의 사전 설정을 사용하는 것이 좋습니다. 사용자 지정 CSS를 적용하여 시각적 사용자 지정을 달성할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드 예입니다.

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**고정 크기 포함 및 응답형 포함**

포함된 모드에서 뷰어가 기존 웹 페이지에 추가되며, 이 페이지에 이미 뷰어와 관련이 없는 일부 고객 콘텐츠가 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지 부동산의 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치를 위한 웹 페이지 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 응답형 웹 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 크기 포함 모드가 사용됩니다. 이 선택 사항은 정적 페이지 레이아웃이 있는 웹 페이지에 가장 적합합니다.

응답형 디자인 포함 모드에서는 컨테이너 `DIV`의 크기 변경에 응답하여 런타임 중에 뷰어의 크기를 조정해야 한다고 가정합니다. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

인라인 확대/축소 뷰어에서 응답형 디자인 포함 모드를 사용할 때는 `imagereload` 매개 변수를 사용하여 기본 보기 이미지에 대한 명시적 중단점을 지정해야 합니다. 가장 좋은 방법은 웹 페이지 CSS에 따라 중단점을 뷰어 너비 중단점과 일치시키는 것입니다.

응답형 디자인 포함 모드에서 뷰어는 웹 페이지 컨테이너 `DIV`의 크기가 어떻게 지정되는지에 따라 다르게 동작합니다. 웹 페이지가 컨테이너 `DIV`의 너비만 설정하고 높이를 제한을 두지 않는 경우 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능은 측면에 패딩되지 않고 자산이 보기에 완벽하게 맞습니다. 이 특정 사용 사례는 Bootstrap 또는 Foundation과 같은 반응형 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적입니다.

그렇지 않으면 웹 페이지가 뷰어의 컨테이너 `DIV`에 대한 너비와 높이를 모두 설정하면 뷰어가 해당 영역만 채우고 웹 페이지 레이아웃에서 제공하는 크기를 따릅니다. 좋은 사용 사례 예제는 뷰어를 모달 오버레이에 포함하고, 이 오버레이는 웹 브라우저 창 크기에 따라 크기가 조정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 `FlyoutViewer.js`를 포함해야 합니다. `FlyoutViewer.js` 표준 IS- [!DNL html5/js/] Viewers 배포의 다음 하위 폴더에 있습니다.

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

뷰어가 Adobe Dynamic Media 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>페이지에서 기본 뷰어 JavaScript `include` 파일만 참조합니다. 런타임 시 뷰어의 논리에 의해 다운로드될 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조하지 마십시오. 특히 `/s7viewers` 컨텍스트 경로(소위 통합 SDK `include`)에서 뷰어가 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오. 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리의 위치가 뷰어의 논리에 의해 완전히 관리되고 뷰어 릴리스 간에 위치가 변경되기 때문입니다. Adobe은 이전 버전의 보조 뷰어 `includes`를 서버에 유지하지 않습니다.
>
>
>따라서 페이지에서 뷰어가 사용하는 보조 JavaScript `include`에 직접 참조를 지정하면 새 제품 버전이 배포될 때 나중에 뷰어 기능이 중단됩니다.

1. 컨테이너 DIV를 정의합니다.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. 이 ID가 나중에 뷰어 API로 전달되므로 DIV 요소에는 해당 ID가 정의되어 있어야 합니다.

   자리 표시자 DIV는 배치된 요소입니다. 즉, `position` CSS 속성이 `relative` 또는 `absolute`로 설정되어 있습니다.

   자리 표시자 DIV 요소에 적절한 `z-index`을 지정하는 것은 웹 페이지의 책임입니다. 이렇게 하면 뷰어의 플라이아웃 부분이 다른 웹 페이지 요소의 맨 위에 표시됩니다.

   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 뷰어 크기를 설정합니다.

   이 뷰어는 여러 항목 세트로 작업할 때 축소판을 표시합니다. 데스크탑 시스템에서는 기본 보기 아래에 축소판이 배치됩니다. 동시에 뷰어에서는 `setAsset()` API를 사용하여 런타임 중에 기본 자산을 교체할 수 있습니다. 개발자는 새 자산에 항목이 하나만 있을 때 뷰어가 하단 영역에서 축소판 영역을 관리하는 방법을 제어할 수 있습니다. 외부 뷰어 크기를 그대로 유지한 다음 기본 보기에서 높이를 늘리고 축소판 영역을 점유할 수 있습니다. 또는 기본 보기 크기를 정적으로 유지하고 외부 뷰어 영역을 축소하여 웹 페이지 컨텐츠를 위로 이동한 다음 축소판에서 남은 사용 가능한 페이지 공간을 사용할 수 있습니다.

   외부 뷰어 제한을 그대로 유지하려면 `.s7flyoutviewer` 최상위 CSS 클래스의 크기를 절대 단위로 정의합니다. CSS의 크기 조절은 HTML 페이지나 사용자 지정 뷰어 CSS 파일에 바로 삽입될 수 있으며 나중에 Dynamic Media Classic의 뷰어 사전 설정 레코드에 할당하거나 스타일 명령을 사용하여 명시적으로 전달할 수 있습니다.

   CSS를 사용하여 뷰어의 스타일을 지정하는 방법에 대한 자세한 내용은 [인라인 확대/축소 뷰어 사용자 지정](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) 을 참조하십시오.

   다음은 HTML 페이지에서 정적 외부 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음 샘플 페이지에서 고정된 외부 뷰어 영역이 있는 동작을 볼 수 있습니다. 세트 간에 전환할 때 외부 뷰어 크기가 변경되지 않습니다.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   기본 보기 차원을 정적으로 만들려면 `.s7flyoutviewer .s7container` CSS 선택기를 사용하여 내부 `Container` SDK 구성 요소에 대한 뷰어 크기를 절대 단위로 정의합니다. 또한 기본 뷰어 CSS의 `.s7flyoutviewer` 최상위 CSS 클래스에 대해 정의된 고정 크기를 `auto` 로 설정하여 재정의해야 합니다.

   다음은 자산을 전환할 때 기본 보기 영역의 크기가 변경되지 않도록 내부 `Container` SDK 구성 요소에 대한 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음 샘플 페이지에는 고정된 기본 보기 크기를 사용하는 뷰어 동작이 표시됩니다. 세트 간에 전환할 때 기본 보기는 정적 상태로 유지되며 웹 페이지 컨텐츠는 세로로 이동합니다.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   또한 기본 뷰어 CSS는 기본 외부 영역에 대해 고정 크기를 제공합니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.FlyoutViewer` 클래스의 인스턴스를 만들고 모든 구성 정보를 해당 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 JSON 개체로 생성자에게 전달됩니다. 최소한, 이 개체에는 뷰어 컨테이너 ID의 이름이 들어 있고 뷰어가 지원하는 구성 매개 변수와 함께 중첩된 `params` JSON 개체가 있는 `containerId` 필드가 있어야 합니다. 이 경우 `params` 개체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL 이상이 있어야 합니다. 초기 자산은 `asset` 매개 변수이고, CSS를 `contentUrl` 매개 변수로 로드하기 위한 기본 경로와, 사전 설정 이름은 `config` 매개 변수로 설정됩니다. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 DOM에 뷰어 컨테이너를 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 `BODY` 태그를 닫기 직전에 또는 body `onload()` 이벤트에서 `init()` 메서드를 호출하십시오.

   동시에 컨테이너 요소가 아직 웹 페이지 레이아웃의 일부일 필요는 없습니다. 예를 들어 지정된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 지연합니다. 이 작업이 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 뷰어 인스턴스를 만드는 예입니다. 이 예제에서는 `inlineZoomViewer`이 뷰어 인스턴스라고 가정합니다. `s7viewer` 은 자리 표시자 `DIV`;의 이름입니다. `http://s7d1.scene7.com/is/image/`은 이미지 제공 URL입니다. 및 `Scene7SharedAssets/ImageSet-Views-Sample`는 자산입니다.

   ```
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   다음 코드는 고정된 크기의 인라인 확대/축소 뷰어를 포함하는 작은 웹 페이지의 전체 예입니다.

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 제한 없는 높이를 사용한 반응형 디자인 포함 {#section-056cb574713c4d07be6d07cf3c598839}

응답형 디자인 포함 기능을 사용할 경우, 일반적으로 웹 페이지에는 뷰어 컨테이너의 런타임 크기를 지시하는 유연한 레이아웃이 있습니다 `DIV`. 다음 예를 들어, 웹 페이지에서 뷰어의 컨테이너 `DIV`가 웹 브라우저 창 크기의 40%를 취할 수 있도록 허용하여 높이 제한이 없는 것으로 가정해 보겠습니다. 웹 페이지 HTML 코드는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 포함 단계와 비슷합니다. 유일한 차이는 기본 뷰어 CSS에서 고정된 크기 조정을 상대 단위로 설정하여 무시해야 한다는 것입니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 다음 세 가지 예외가 포함된 고정 크기 포함과 동일합니다.

* 기존 &quot;holder&quot; `DIV`에 컨테이너 `DIV`를 추가합니다.
* 명시적 중단점이 있는 `imagereload` 매개 변수를 추가했습니다.
* 절대 단위를 사용하여 고정 뷰어 크기를 설정하는 대신 다음과 같이 뷰어 `width` 및 `height`을 100%로 설정하는 CSS를 사용합니다.

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

다음 코드는 완전한 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되고 뷰어 종횡비가 자산과 어떻게 일치하는지 확인합니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

다음 예제 페이지에서는 제한 높이가 있는 반응형 디자인 포함의 실제 사용을 보여 줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[대체 데모 위치](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 폭과 높이가 정의된 유연한 크기 포함 {#section-0a329016f9414d199039776645c693de}

너비와 높이가 정의된 유연한 크기가 있는 경우 웹 페이지 스타일링이 다릅니다. 이 확장은 `"holder"` DIV에 두 크기를 모두 제공하고 브라우저 창에 배치합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

나머지 포함 단계는 제한 높이가 없는 응답형 디자인 포함에 사용되는 단계와 동일합니다. 결과 예는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Setter 기반 API를 사용하여 포함 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 이 API 생성자를 사용하면 매개 변수를 사용하지 않으며 구성 매개 변수는 별도의 JavaScript 호출과 함께 `setContainerId()`, `setParam()` 및 `setAsset()` API 메서드를 사용하여 지정합니다.

다음 예에서는 setter 기반 API와 함께 고정 크기 포함 사용을 보여 줍니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```
