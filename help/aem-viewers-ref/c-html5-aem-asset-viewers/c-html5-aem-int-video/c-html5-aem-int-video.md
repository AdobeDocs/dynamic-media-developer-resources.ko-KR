---
description: 대화형 비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다.
seo-description: 대화형 비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다.
seo-title: 인터랙티브한 비디오
solution: Experience Manager
title: 인터랙티브한 비디오
topic: Dynamic media
uuid: 116c6b40-2490-4f1a-9c76-e06082069cc8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# 인터랙티브한 비디오{#interactive-video}

대화형 비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다.

뷰어 뷰어는 비디오 콘텐트 옆에 대화형 제품 견본도 표시합니다. 단일 비디오 및 응용 비디오 집합이 모두 지원됩니다. HTML5 비디오를 지원하는 데스크탑 및 모바일 웹 브라우저에서 작동하도록 설계되었습니다. 뷰어는 비디오 컨텐츠, 비디오 장(chapter) 탐색 및 소셜 공유 도구 위에 표시되는 선택적 자막을 지원합니다. 이 뷰어의 목적은 &quot;쇼퍼블 비디오&quot; 경험을 구현하는 데 도움이 됩니다. 즉, 사용자는 특정 비디오 시간 영역과 연관된 견본을 선택하고 고객 웹 사이트의 빠른 보기 또는 제품 세부 사항 페이지로 리디렉션할 수 있습니다.

뷰어 유형은 510입니다.

## 데모 URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

and

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## 시스템 요구 사항 {#section-b7270cc4290043399681dc504f043609}

시스템 [요구 사항을](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)참조하십시오.

## 대화형 비디오 뷰어 사용 {#section-e6c68406ecdc4de781df182bbd8088b4}

대화형 비디오 뷰어는 런타임 시 뷰어가 다운로드한 기본 JavaScript 파일 및 도우미 파일 집합(단일 JavaScript는 이 특정 뷰어, 자산 및 CSS에서 사용하는 모든 뷰어 SDK 구성 요소에 포함)을 나타냅니다.

대화형 비디오 뷰어는 이미지 제공 뷰어와 함께 제공되는 프로덕션 준비 HTML 페이지를 사용하여 팝업 모드에서 사용할 수 있습니다. 또한 내장 모드에서 사용할 수 있으며, 이 모드에서는 문서화된 API를 사용하여 타깃팅된 웹 페이지에 통합됩니다.

구성 및 스키닝은 이 안내서에서 설명하는 다른 뷰어와 유사합니다. 모든 스키닝은 사용자 정의(CSS) CSS(Cascading Style Sheet)를 통해 가능합니다.

모든 [뷰어에 공통으로 사용되는 명령 참조 - 구성 특성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어 - URL에 공통되는 명령 참조](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 인터랙티브한 비디오 뷰어를 사용한 인터랙션 {#section-642e66ca38cd4032992840ec6c0b0cd2}

대화형 비디오 뷰어는 재생/일시 중지 단추, 비디오 스크러버, 비디오 시간 버블, 재생 시간/총 시간 표시기, 볼륨 컨트롤, 전체 화면 단추, 닫힌 캡션 전환 등과 같은 비디오 재생을 위한 표준 사용자 인터페이스 컨트롤 세트를 제공합니다. 이러한 모든 컨트롤은 기본 보기 바로 아래에 컨트롤 막대로 그룹화됩니다.

터치 장치에서는 장치의 하드웨어 단추를 사용해서만 볼륨을 제어할 수 있으므로 볼륨 컨트롤이 사용자 인터페이스에서 숨겨집니다.

뷰어가 팝업 모드에서 작동하면 사용자 인터페이스에서 전체 화면 단추를 사용할 수 없습니다.

뷰어는 비디오 보기 영역 오른쪽에 대화형 색상 견본이 있는 패널을 표시합니다. 비디오가 재생되면 견본 목록이 자동으로 진행되므로 현재 비디오 영역에 해당하는 견본이 표시됩니다. 견본을 클릭하거나 탭하면 작성자 시간 동안 해당 견본과 연관된 동작이 트리거됩니다. 설정 방법에 따라 트리거가 웹 사이트의 다른 페이지로 리디렉션되거나 제품 정보를 웹 페이지 로직으로 다시 전달할 수 있으므로 관련 제품 컨텐츠를 표시하는 빠른 보기를 열 수 있습니다.

비디오 장(chapter)이 활성화되면 비디오 컨텐츠를 빠르게 탐색할 수 있습니다. 비디오 장은 비디오 스크러버 트랙에 마커로 표시되며 롤오버(또는 터치 시스템에서 한 번 누르기)에 장 제목과 설명을 표시합니다. 고객은 장 마커를 클릭하거나 장 설명 버블을 탭하여 특정 장을 &quot;검색&quot;할 수 있습니다.

뷰어는 다양한 소셜 미디어 공유 도구도 지원합니다. 사용자 인터페이스에서 사용자가 클릭하거나 탭하면 공유 도구 모음으로 확장되는 단일 단추로 사용할 수 있습니다. 공유 도구 모음에는 Facebook, Twitter, 이메일 공유, 포함 코드 공유 및 링크 공유와 같이 지원되는 각 공유 채널 유형에 대한 아이콘이 포함되어 있습니다. 이메일 공유, 포함 공유 또는 링크 공유 도구가 활성화되면 뷰어는 해당 데이터 입력 양식이 있는 모달 대화 상자를 표시합니다. Facebook 또는 Twitter가 호출되면 뷰어는 소셜 미디어 서비스에서 사용자를 표준 공유 대화 상자로 리디렉션합니다. 또한 공유 도구가 활성화되면 비디오 재생이 자동으로 일시 중지됩니다. 웹 브라우저 보안 제한 때문에 전체 화면 모드에서 공유 도구를 사용할 수 없습니다.

뷰어는 키보드로 완벽하게 액세스할 수 있습니다. 키보드 [접근성 및 탐색을](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)참조하십시오.

## 대화형 비디오 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

대화형 비디오 뷰어는 호스팅 페이지에 포함되도록 디자인되었습니다. 이러한 웹 페이지에는 정적 레이아웃이 있거나, &quot;응답 속도&quot;가 있을 수 있으며, 다른 장치 또는 서로 다른 브라우저 창 크기에 대해 다르게 표시될 수 있습니다.

이러한 요구 사항을 수용하기 위해 뷰어는 두 가지 기본 작업 모드를 지원합니다.고정 크기 임베드 및 반응형 임베드.

**고정 크기 임베드 모드 및 반응형 디자인 임베드 모드 정보**

내장 모드에서 뷰어는 기존 웹 페이지에 추가되며, 여기에는 뷰어와 관련이 없는 일부 고객 컨텐츠가 이미 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지의 부동산의 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치의 웹 페이지 지향 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 반응형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 크기 임베딩이 사용됩니다. 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 임베드에서는 컨테이너의 크기 변경에 응답하여 런타임 시 뷰어의 크기를 조정해야 할 수 있다고 가정합니다 `DIV`. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

반응형 디자인 임베드 모드에서 뷰어는 웹 페이지의 컨테이너 크기 조절 방식에 따라 다르게 동작합니다 `DIV`. 웹 페이지가 컨테이너의 너비만 설정하고 높이를 제한을 두지 `DIV`않으면 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능을 사용하면 측면에 패딩 없이 에셋이 보기에 완벽하게 맞춰집니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 웹 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적으로 사용됩니다.

그렇지 않으면 웹 페이지가 뷰어의 컨테이너 너비와 높이를 모두 설정하는 경우 뷰어는 해당 `DIV`영역만 채우고 웹 페이지 레이아웃이 제공하는 크기를 따릅니다. 예를 들어 뷰어를 모달 오버레이에 포함시켜 오버레이의 크기가 웹 브라우저 창 크기에 따라 조정되는 것이 좋습니다.

**고정 크기 임베드**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. 컨테이너를 `DIV`정의합니다.
1. 뷰어 크기 설정
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 포함해야 [!DNL InterativeVideoViewer.js]합니다. 이 [!DNL InteractiveVideoViewer.js] 파일은 표준 IS-뷰어 배포의 [!DNL html5/js/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않은 경우 IS-뷰어가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>페이지에서 기본 뷰어 JavaScript `include` 파일만 참조해야 합니다. 런타임 시 뷰어의 논리로 다운로드될 수 있는 추가 JavaScript 파일을 웹 페이지 코드에서 참조해서는 안 됩니다. 특히, 컨텍스트 경로(소위 통합 SDK)에서 뷰어가 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오 `/s7viewers` `include`. 이유는 런타임 뷰어 라이브러리의 위치 `Utils.js` 또는 유사한 위치는 뷰어의 논리로 완전히 관리되고 뷰어 릴리스 간에 위치가 변경되기 때문입니다. Adobe는 이전 버전의 보조 뷰어를 서버에 보관하지 않습니다. `includes`
>
>
>따라서 페이지에서 뷰어가 `include` 사용하는 보조 JavaScript에 직접 참조를 지정하면 새 제품 버전이 배포될 때 나중에 뷰어 기능이 중단됩니다.

1. 컨테이너를 `DIV`정의합니다.

   뷰어를 표시할 페이지에 빈 `DIV` 요소를 추가합니다. 이 `DIV` ID는 나중에 뷰어 API로 전달되므로 요소의 ID가 정의되어 있어야 합니다. DIV의 크기는 CSS를 통해 지정됩니다.

   자리 표시자는 배치된 `DIV` 요소로서, 즉 CSS `position` 속성이 `relative` 또는 `absolute`로 설정되어 있습니다.

   전체 화면 기능이 Internet Explorer에서 제대로 작동하려면 DOM에 자리 표시자보다 높은 스택 순서가 있는 다른 요소가 없는지 확인합니다 `DIV`.

   다음은 정의된 자리 표시자 `DIV` 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 뷰어 크기 설정

   뷰어의 정적 크기를 절대 단위로 `.s7interactivevideoviewer` 최상위 CSS 클래스에 대해 선언하거나 `stagesize` 수정자를 사용하여 설정할 수 있습니다.

   HTML 페이지 또는 사용자 정의 뷰어 CSS 파일에서 바로 크기를 CSS로 지정할 수 있습니다. 이 파일은 나중에 AEM Assets의 뷰어 사전 설정 레코드에 지정되거나, 주문형 `style` 명령을 사용하여 명시적으로 전달됩니다.

   CSS를 [사용하여](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 뷰어의 스타일 지정에 대한 자세한 내용은 대화형 비디오 뷰어 사용자 지정을 참조하십시오.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   AEM Assets - on-demand의 뷰어 사전 설정 레코드에 `stagesize` 수정자를 설정할 수 있습니다. 또는 다음과 같이 `params` 컬렉션을 통해 뷰어 초기화 코드를 명시적으로 전달하거나 명령 참조 섹션에 설명된 대로 API 호출로 전달할 수 있습니다.

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   CSS 기반 접근 방식이 권장되며 이 예제에서 사용됩니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.InteractiveVideoViewer` 클래스 인스턴스를 만들고, 모든 구성 정보를 생성자에 전달하고, 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 생성자에게 JSON 개체로 전달됩니다. 최소한 이 개체에는 뷰어에서 지원하는 구성 매개 변수와 함께 뷰어 컨테이너 ID의 이름과 중첩된 `containerId` `params` JSON 개체가 있는 필드가 있어야 합니다.

   이 경우 `params` 개체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL 이상이 있어야 하며 초기 자산은 `asset` 매개 변수로 전달되어야 합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행, 속성으로 전달된 비디오 서버 URL, 매개 변수로 초기 에셋, `videoserverurl` `asset` `interactivedata` 속성으로 대화형 데이터를 사용하여 뷰어를 만들고 시작할 수 있습니다. JSON 기반 초기화 API를 사용하면 단일 코드 행을 사용하여 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 닫는 `init()` 태그 바로 앞 또는 body `BODY` `onload()` 이벤트에서 메서드를 호출합니다.

   이와 마찬가지로 컨테이너 요소가 아직 웹 페이지 레이아웃의 일부일 필요는 없습니다. 예를 들어, 지정된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 지연합니다. 이러한 경우 뷰어 부하가 자동으로 다시 시작됩니다.

   다음은 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 뷰어 인스턴스를 만드는 예입니다. 이 예에서는 다음을 가정합니다.

   * 뷰어 인스턴스는 `interactiveVideoViewer`입니다.
   * 자리 표시자의 이름은 `DIV` 입니다 `s7viewer`.
   * 이미지 제공 URL은 `https://aodmarketingna.assetsadobe.com/is/image/`입니다.
   * 비디오 서버 URL은 `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`입니다.
   * 콘텐트 URL은 `https://aodmarketingna.assetsadobe.com/`입니다.
   * 자산이 `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`표시됩니다.
   * 인터랙티브한 데이터는 `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`다음과 같습니다.

   ```
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   다음 코드는 고정된 크기의 대화형 비디오 뷰어를 포함하는 간단한 웹 페이지의 전체 예입니다.

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**제한 없는 높이로 반응형 디자인 임베드**

반응형 디자인 임베드에서는 일반적으로 웹 페이지에 뷰어의 컨테이너 런타임 크기를 지정하는 유연한 레이아웃이 `DIV`있습니다. 다음 예에서는 웹 페이지에서 뷰어의 컨테이너에 웹 브라우저 창 크기의 40% `DIV` 를 적용하고 높이를 제한을 두지 않는다고 가정합니다. 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 임베드 단계와 유사합니다. 유일한 차이점은 뷰어 크기를 명시적으로 정의할 필요가 없다는 것입니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. 컨테이너 DIV를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 임베딩과 동일합니다. 컨테이너 DIV를 기존 DIV에 `"holder"` 추가합니다. 다음 코드는 전체 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되고 뷰어 종횡비가 자산과 어떻게 일치하는지 확인합니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

다음 예제 페이지에서는 제한 없는 높이와 함께 반응형 디자인 임베딩의 실제 사용을 보여줍니다.

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**폭 및 높이가 정의된 응답형 포함**

너비와 높이가 정의된 응답형 임베드의 경우 웹 페이지 스타일이 다릅니다. DIV에 두 가지 크기를 `"holder"` 제공하고 브라우저 창에서 가운데에 표시합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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

나머지 임베드 단계는 무제한 높이로 임베드하는 데 사용되는 단계와 동일합니다. 결과 예는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter 기반 API를 사용하여 포함**

JSON 기반 초기화를 사용하는 대신 setter 기반 API와 인수 없음 생성자를 사용할 수 있습니다. 이 API 생성자를 사용하면 매개 변수를 사용하지 않으며 별도의 JavaScript 호출과 함께 `setContainerId()`API `setParam()`및 `setAsset()` API 메서드를 사용하여 구성 매개 변수를 지정할 수 있습니다.

다음 예제에서는 setter 기반 API와 함께 고정 크기 임베드 사용을 보여 줍니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```

