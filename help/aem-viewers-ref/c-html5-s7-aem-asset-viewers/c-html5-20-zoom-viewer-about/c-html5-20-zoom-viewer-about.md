---
title: 확대/축소
description: 확대/축소 뷰어는 확대/축소 가능한 이미지를 표시하는 이미지 뷰어입니다. 이 뷰어는 이미지 세트에서 작동하며 색상 견본을 사용하여 탐색합니다. 확대/축소 도구, 전체 화면 지원, 색상 견본 및 선택적 닫기 버튼이 있습니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.
keywords: 반응형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2343'
ht-degree: 0%

---

# 확대/축소{#zoom}

확대/축소 뷰어는 확대/축소 가능한 이미지를 표시하는 이미지 뷰어입니다. 이 뷰어는 이미지 세트에서 작동하며 색상 견본을 사용하여 탐색합니다. 확대/축소 도구, 전체 화면 지원, 색상 견본 및 선택적 닫기 버튼이 있습니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형 502.

[시스템 요구 사항 및 필수 구성 요소](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)를 참조하십시오.

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 확대/축소 뷰어 사용 {#section-e6c68406ecdc4de781df182bbd8088b4}

확대/축소 뷰어는 런타임에 뷰어가 다운로드한 기본 JavaScript 파일 및 도우미 파일 세트(단일 JavaScript에 이 특정 뷰어, 에셋, CSS에서 사용하는 모든 뷰어 SDK 구성 요소가 포함됨)를 나타냅니다.

IS-Viewer와 함께 제공된 프로덕션 준비 HTML 페이지를 사용하여 팝업 모드에서 또는 문서화된 API를 사용하여 대상 웹 페이지에 통합된 임베드 모드에서 확대/축소 뷰어를 사용할 수 있습니다.

구성 및 스키닝은 다른 뷰어의 것과 유사합니다. 모든 스키닝은 사용자 지정 CSS를 통해 수행됩니다.

[모든 뷰어에 공통되는 명령 참조 - 구성 특성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)을 참조하십시오.

## 확대/축소 뷰어와 상호 작용 {#section-642e66ca38cd4032992840ec6c0b0cd2}

확대/축소 뷰어는 다른 모바일 애플리케이션에서 일반적인 다음 터치 제스처를 지원합니다. 뷰어가 사용자의 스와이프 제스처를 처리할 수 없는 경우 이벤트를 웹 브라우저에 전달하여 기본 페이지 스크롤을 수행합니다. 이러한 기능을 사용하면 뷰어가 장치 화면 영역의 대부분을 차지하는 경우에도 페이지를 탐색할 수 있습니다.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>제스처 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>한 번 탭 </p> </td> 
   <td colname="col2"> <p> 견본에서 새 썸네일을 선택합니다. 기본 보기에서는 사용자 인터페이스 요소를 숨기거나 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>두 번 탭 </p> </td> 
   <td colname="col2"> <p> 최대 확대율에 도달할 때까지 한 레벨로 확대합니다. 다음 더블 탭 제스처는 뷰어를 초기 시청 상태로 재설정한다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>핀치 </p> </td> 
   <td colname="col2"> <p>확대하거나 축소합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수평 밀기 또는 튀기기 </p> </td> 
   <td colname="col2"> <p> 견본 막대의 견본 목록을 스크롤합니다. </p> <p> 이미지가 재설정 상태이고 <span class="codeph"> frametransition </span> 매개 변수가 slide로 설정되어 있으면 슬라이드 애니메이션으로 에셋이 변경됩니다. 다른 <span class="codeph"> frametransition </span> 모드의 경우 제스처는 기본 페이지 스크롤을 수행합니다. </p> <p> 이미지가 확대되면 이미지가 가로로 이동합니다. 이미지가 뷰 에지로 이동되고 동일한 방향으로 스와이프가 수행되는 경우, 제스처는 네이티브 페이지 스크롤링을 수행한다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수직 스와이프 </p> </td> 
   <td colname="col2"> <p> 이미지가 재설정 상태이면, 제스처는 네이티브 페이지 스크롤링을 수행한다. </p> <p> 이미지가 확대되면 이미지가 세로로 이동합니다. 이미지가 뷰 에지로 이동되고 동일한 방향으로 스와이프가 수행되는 경우, 제스처는 네이티브 페이지 스크롤을 수행한다. </p> <p> 제스처가 견본 영역 내에서 이루어지면 기본 페이지 스크롤이 수행됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

뷰어는 터치 스크린 및 마우스로 Windows 장치에서 터치 입력 및 마우스 입력을 모두 지원합니다. 그러나 이 지원은 Chrome, Internet Explorer 11 및 Edge 웹 브라우저로만 제한됩니다.

이 뷰어는 키보드에 완전히 액세스할 수 있습니다.

[키보드 접근성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)을 참조하세요.

## 확대/축소 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 동작에 대한 요구 사항이 다릅니다. 경우에 따라 웹 페이지에서 링크를 제공하여 선택하면 뷰어가 별도의 브라우저 창에서 열립니다. 다른 경우에는 뷰어를 호스팅 페이지에 직접 임베드해야 합니다. 후자의 경우, 웹 페이지는 정적 레이아웃을 가질 수도 있고, 디바이스마다 또는 브라우저 창 크기마다 다르게 표시되는 반응형 디자인을 사용할 수도 있습니다. 이러한 요구를 수용하기 위해 뷰어는 팝업, 고정 크기 임베딩 및 응답형 디자인 임베딩의 세 가지 기본 작업 모드를 지원합니다.

**팝업 모드 정보**

팝업 모드에서는 뷰어가 별도의 웹 브라우저 창 또는 탭에서 열립니다. 브라우저 크기가 조정되거나 디바이스 방향이 변경되는 경우 전체 브라우저 창 영역을 가져와서 조정합니다.

이 모드는 모바일 장치에서 가장 일반적입니다. 웹 페이지는 `window.open()` JavaScript 호출, 올바르게 구성된 `A` HTML 요소 또는 기타 적절한 메서드를 사용하여 뷰어를 로드합니다.

팝업 작업 모드에서는 기본 HTML 페이지를 사용하는 것이 좋습니다. 기본 HTML 페이지는 `ZoomViewer.html`이라고 하며 다음과 같이 표준 IS-Viewers 배포의 `html5/` 하위 폴더 아래에 있습니다.

`<s7viewers_root>/html5/ZoomViewer.html`

사용자 지정 CSS를 적용하여 페이지에 맞게 사용자 지정된 모양을 만듭니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**고정 크기 포함 모드 및 반응형 디자인 포함 모드 정보**

임베드된 모드에서는 뷰어가 기존 웹 페이지에 추가되며, 이 페이지에는 뷰어와 관련이 없는 고객 콘텐츠가 이미 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지의 부동산의 일부만 점유한다.

주요 사용 사례는 데스크탑 또는 태블릿 장치를 위한 웹 페이지 지향적이며, 또한 디바이스 유형에 따라 레이아웃을 자동으로 조정하는 응답형 디자인 페이지입니다.

고정 크기 임베딩은 뷰어가 초기 로드 후 크기를 변경하지 않을 때 사용됩니다. 이 옵션은 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 포함 모드에서는 컨테이너 `DIV`의 크기 변경으로 인해 런타임 중에 뷰어의 크기 조정이 필요하다고 가정합니다. 가장 일반적인 사용 사례는 유연한 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

반응형 디자인 포함 모드에서 뷰어는 웹 페이지의 컨테이너 크기 `DIV` 방식에 따라 다르게 동작합니다. 웹 페이지에서 `DIV` 컨테이너의 너비만 설정하고 높이는 제한되지 않은 경우 뷰어는 사용된 에셋의 종횡비에 따라 높이를 자동으로 선택합니다. 이 논리는 에셋이 측면에 패딩이 없이 보기에 완벽하게 맞는지 확인합니다. 이 사용 사례는 Bootstrap 및 Foundation과 같은 반응형 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적으로 사용됩니다.

웹 페이지에서 뷰어의 컨테이너 `DIV`에 대한 너비와 높이를 모두 설정하면 뷰어가 해당 영역을 채우고 웹 페이지에서 제공하는 크기를 따릅니다. 예를 들어, 웹 브라우저 창 크기에 따라 오버레이의 크기가 조정되는 모달 오버레이에 뷰어를 포함합니다.

## 고정 크기 포함 {#section-44f365e6c0dd40709467a459afa82a7f}

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 DIV 정의.
1. 뷰어 크기를 설정하는 중입니다.
1. 뷰어를 만들고 초기화하는 중입니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 [!DNL ZoomViewer.js]을(를) 포함해야 합니다. [!DNL ZoomViewer.js] 파일은 표준 IS-Viewers 배포의 [!DNL html5/js/] 하위 폴더에 있습니다.

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewer가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>페이지의 기본 뷰어 JavaScript `include` 파일만 참조합니다. 런타임 시 뷰어의 논리로 다운로드할 수 있는 웹 페이지 코드에 있는 추가 JavaScript 파일을 참조하지 마십시오. 특히 `/s7viewers` 컨텍스트 경로(통합 SDK `include`이라고 함)에서 뷰어가 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오. 그 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리의 위치가 뷰어의 논리에 의해 완전히 관리되고 뷰어 릴리스 간 위치가 변경되기 때문입니다. Adobe이 서버에 이전 버전의 보조 뷰어 `includes`을(를) 보관하지 않습니다.
>
>
>따라서 뷰어가 사용하는 보조 JavaScript `include`을(를) 페이지에서 직접 참조하면 나중에 새 제품 버전을 배포할 때 뷰어 기능이 중단됩니다.

1. 컨테이너 DIV 정의.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. DIV 요소의 ID는 나중에 뷰어 API로 전달되므로 이 ID가 정의되어 있어야 합니다.

   자리 표시자 DIV는 위치 요소입니다. 즉 `position` CSS 속성이 `relative` 또는 `absolute`(으)로 설정되어 있습니다.

   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 뷰어 크기를 설정하는 중입니다.

   이 뷰어는 여러 항목 세트로 작업할 때 썸네일을 표시하며, 데스크톱 시스템에서는 썸네일이 기본 보기 아래에 배치됩니다. 동시에 뷰어는 `setAsset()` API를 사용하여 런타임에 기본 자산을 교환할 수 있습니다. 개발자는 새 에셋에 항목이 하나만 있을 때 맨 아래에 있는 썸네일 영역을 뷰어가 관리하는 방법을 제어할 수 있습니다. 외부 뷰어 크기를 그대로 유지하고 기본 보기에서 높이를 늘리고 썸네일 영역을 차지하도록 할 수 있습니다. 또는 기본 보기 크기를 정적으로 유지하고 외부 뷰어 영역을 축소하여 웹 페이지 콘텐츠를 위로 이동하고 썸네일에서 남은 자유 화면 공간을 사용할 수 있습니다.

   외부 뷰어 경계를 그대로 유지하려면 `.s7zoomviewer` 최상위 CSS 클래스의 크기를 절대 단위로 정의합니다. CSS의 크기 조정은 HTML 페이지에 바로 지정할 수 있습니다. 또는 나중에 Dynamic Media Classic의 뷰어 사전 설정 레코드에 할당되거나 스타일 명령을 사용하여 명시적으로 전달되는 사용자 지정 뷰어 CSS 파일에 배치할 수 있습니다.

   CSS를 사용하여 뷰어를 스타일링하는 방법에 대한 자세한 내용은 [확대/축소 뷰어 사용자 지정](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)을 참조하십시오.

   다음은 HTML 페이지에서 정적 외부 뷰어 크기를 정의하는 예제입니다.

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음 예제에서는 고정된 바깥쪽 뷰어로 동작을 확인할 수 있습니다. 세트 간에 전환할 때 외부 뷰어 크기는 변경되지 않습니다.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   기본 보기 차원을 정적으로 설정하려면 `.s7zoomviewer` `.s7container` CSS 선택기를 사용하거나 `stagesize` 수정자를 사용하여 내부 `Container` SDK 구성 요소에 대한 뷰어 크기를 절대 단위로 정의합니다.

   다음은 자산을 전환할 때 기본 보기 영역의 크기가 변경되지 않도록 내부 `Container` SDK 구성 요소의 뷰어 크기를 정의하는 예입니다.

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음 데모 페이지에는 기본 보기 크기가 고정된 뷰어 동작이 표시됩니다. 세트 간에 전환하면 기본 보기는 정적인 상태로 유지되며 웹 페이지 콘텐츠가 세로로 이동합니다.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   Dynamic Media Classic의 뷰어 사전 설정 레코드에서 `stagesize` 한정자를 설정할 수 있습니다. 또는 다음과같이 이 도움말의 명령 참조 섹션에 설명된 대로 `params` 컬렉션을 사용하는 뷰어 초기화 코드로 명시적으로 전달하거나 API 호출로 전달할 수 있습니다.

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   CSS 기반 접근 방식이 권장되며 이 예제에서 사용됩니다.

1. 뷰어를 만들고 초기화하는 중입니다.

   위의 단계를 완료하면 `s7viewers.ZoomViewer` 클래스의 인스턴스를 만들고 모든 구성 정보를 해당 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다.

   구성 정보는 JSON 개체로 생성자에 전달됩니다. 최소한 이 개체에는 뷰어 컨테이너 ID의 이름을 포함하는 `containerId` 필드와 뷰어가 지원하는 구성 매개 변수와 함께 중첩된 `params` JSON 개체가 있어야 합니다. 이 경우 `params` 개체에는 최소한 `serverUrl` 속성으로 전달된 이미지 제공 URL과 `asset` 매개 변수로 전달된 초기 자산이 있어야 합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 빌드를 지연합니다. 호환성을 최대화하려면 `BODY` 태그를 닫기 직전에 또는 본문 `onload()` 이벤트에서 `init()` 메서드를 호출하십시오.

   동시에 컨테이너 요소는 아직 웹 페이지 레이아웃의 일부가 아니어야 합니다. 예를 들어 할당된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져오는 순간까지 초기화 프로세스를 지연합니다. 이 작업이 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에 전달하고 `init()` 메서드를 호출하는 예입니다. 이 예제에서는 `zoomViewer`이(가) 뷰어 인스턴스이고, `s7viewer`이(가) 자리 표시자 DIV의 이름이고, `http://s7d1.scene7.com/is/image/`이(가) 이미지 제공 URL이고, `Scene7SharedAssets/ImageSet-Views-Sample`이(가) 자산이라고 가정합니다.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   다음 코드는 비디오 뷰어를 고정 크기로 임베드하는 간단한 웹 페이지의 전체 예입니다.

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 무제한 높이의 응답형 디자인 임베딩 {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

응답형 디자인 임베딩을 사용하면 일반적으로 웹 페이지에는 뷰어의 컨테이너 `DIV`의 런타임 크기를 지정하는 일종의 유연한 레이아웃이 있습니다. 다음 예제에서는 웹 페이지에서 뷰어의 컨테이너 `DIV`이(가) 웹 브라우저 창 크기의 40%를 차지하도록 허용하고 높이는 제한되지 않는다고 가정합니다. 웹 페이지 HTML 코드는 다음과 같습니다.

```html {.line-numbers}
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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 임베딩 단계와 유사합니다. 유일한 차이점은 뷰어 크기를 명시적으로 정의할 필요가 없다는 것입니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 DIV 정의.
1. 뷰어를 만들고 초기화하는 중입니다.

위의 모든 단계는 고정 크기 포함과 동일합니다. 기존 `"holder"` DIV에 컨테이너 DIV를 추가합니다. 다음 코드는 완전한 예입니다. 브라우저의 크기를 조정할 때 뷰어 크기가 어떻게 변경되는지, 뷰어 종횡비가 에셋과 어떻게 일치하는지 확인합니다.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

다음 예제 페이지에서는 무제한 높이를 사용하는 응답형 디자인 포함의 보다 실제 사용을 보여 줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 폭 및 높이가 정의된 유연한 크기 포함 {#section-3674e6c032594441a6576b7fb1de6e64}

폭과 높이가 정의된 유연한 크기의 포함이 있는 경우 웹 페이지 스타일이 다릅니다. 두 크기를 `"holder"` DIV에 제공하고 브라우저 창에서 가운데로 맞춥니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

```html {.line-numbers}
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

임베딩 단계의 나머지 부분은 제한되지 않은 높이를 갖는 응답형 디자인 임베딩에 사용되는 단계와 동일합니다. 결과 예제는 다음과 같습니다.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## setter 기반 API를 사용하여 포함 {#section-44e014925f24418b900696003855c0a9}

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 이 API 생성자를 사용하면 매개 변수를 사용하지 않으며, 별도의 JavaScript 호출과 함께 `setContainerId()`, `setParam()` 및 `setAsset()` API 메서드를 사용하여 구성 매개 변수를 지정합니다.

다음 예제에서는 setter 기반 API에 고정 크기 임베딩을 사용하는 방법을 보여 줍니다.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
