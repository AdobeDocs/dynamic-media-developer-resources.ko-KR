---
title: 대화형 비디오
description: 대화형 비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2211'
ht-degree: 0%

---

# 대화형 비디오{#interactive-video}

대화형 비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다.

또한 뷰어에는 비디오 컨텐츠 옆에 대화형 제품 색상 견본도 표시됩니다. 단일 비디오 및 응용 비디오 세트가 모두 지원됩니다. HTML5 비디오를 지원하는 데스크탑 및 모바일 웹 브라우저에서 작동하도록 디자인되었습니다. 뷰어는 비디오 컨텐츠, 비디오 장 탐색 및 소셜 공유 도구 위에 표시되는 선택적 닫힌 캡션을 지원합니다. 이 뷰어의 목적은 &quot;쇼퍼블 비디오&quot; 경험을 구현하는 데 도움이 되는 것입니다. 즉, 사용자는 특정 비디오 시간 영역과 연관된 견본을 선택하고 고객 웹 사이트의 제품 세부 사항 페이지나 Quickview로 리디렉션할 수 있습니다.

뷰어 유형은 510입니다.

## 데모 URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

및

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## 시스템 요구 사항 {#section-b7270cc4290043399681dc504f043609}

자세한 내용은 [시스템 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 대화형 비디오 뷰어 사용 {#section-e6c68406ecdc4de781df182bbd8088b4}

대화형 비디오 뷰어는 런타임에 뷰어가 다운로드한 기본 JavaScript 파일과 도우미 파일 집합을 나타냅니다. 단일 JavaScript는 이 특정 뷰어, 자산 및 CSS에서 사용하는 모든 Viewer SDK 구성 요소에 포함되어 있습니다.

대화형 비디오 뷰어는 이미지 제공 뷰어와 함께 제공된 프로덕션 준비 HTML 페이지를 사용하여 팝업 모드에서 사용할 수 있습니다. 포함된 모드에서 사용할 수도 있으며, 이 모드에서는 문서화된 API를 사용하여 타깃팅된 웹 페이지에 통합됩니다.

구성 및 스키닝은 이 안내서에서 설명하는 다른 뷰어의 구성과 유사합니다. 모든 스키닝은 사용자 지정(CSS) 계단식 스타일 시트를 통해 수행됩니다.

자세한 내용은 [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 대화형 비디오 뷰어와 상호 작용 {#section-642e66ca38cd4032992840ec6c0b0cd2}

대화형 비디오 뷰어는 재생/일시 정지 단추, 비디오 스크러버, 비디오 시간 버블, 재생 시간/총 시간 표시기, 볼륨 제어, 전체 화면 단추 및 닫힌 캡션 토글과 같은 비디오 재생에 대한 표준 사용자 인터페이스 컨트롤 집합을 제공합니다. 이러한 모든 컨트롤은 기본 보기 바로 아래에 컨트롤 막대로 그룹화됩니다.

터치 장치에서는 장치의 하드웨어 단추를 사용해서만 볼륨을 제어할 수 있으므로 볼륨 컨트롤이 사용자 인터페이스에서 숨겨집니다.

뷰어가 팝업 모드에서 작동하면 사용자 인터페이스에서 전체 화면 단추를 사용할 수 없습니다.

뷰어에는 비디오 보기 영역 오른쪽에 대화형 색상 견본이 있는 패널이 표시됩니다. 비디오 재생에 따라 색상 견본 목록이 자동으로 진행되므로 현재 비디오 영역에 해당하는 색상 견본이 표시됩니다. 견본을 클릭하거나 탭하면 작성 시간 동안 그러한 견본과 연관된 작업이 트리거됩니다. 트리거는 설정 방법에 따라 웹 사이트의 다른 페이지로 리디렉션할 수 있습니다. 또는 제품 정보를 다시 웹 페이지 로직에 전달하여 관련 제품 콘텐츠를 표시하는 Quickview의 열기를 트리거할 수 있습니다.

비디오 장 활성화 시 비디오 컨텐츠를 빠르게 탐색할 수 있습니다. 비디오 장은 비디오 스크러버 트랙에 마커로 표시되고 롤오버(또는 터치 시스템의 한 탭에서)에 대한 장 제목과 설명을 표시합니다. 고객은 장 마커를 클릭하거나 장 설명 버블을 탭하여 특정 장을 &quot;찾기&quot;할 수 있습니다.

뷰어는 다양한 소셜 미디어 공유 도구도 지원합니다. 사용자 인터페이스에서 사용자가 클릭하거나 탭할 때 공유 도구 모음으로 확장되는 단일 단추로 사용할 수 있습니다. 공유 도구 모음에는 Facebook, Twitter, 이메일 공유, 포함 코드 공유 및 링크 공유와 같이 지원되는 각 유형의 공유 채널에 대한 아이콘이 포함되어 있습니다. 전자 메일 공유, 포함 공유 또는 링크 공유 도구가 활성화되면 뷰어에 해당 데이터 입력 양식이 있는 모달 대화 상자가 표시됩니다. facebook 또는 Twitter이 호출되면 뷰어는 소셜 미디어 서비스에서 표준 공유 대화 상자로 사용자를 리디렉션합니다. 또한 공유 도구가 활성화되면 비디오 재생이 자동으로 일시 중지됩니다. 웹 브라우저 보안 제한 사항으로 인해 전체 화면 모드에서는 공유 도구를 사용할 수 없습니다.

뷰어는 키보드로 액세스할 수 있습니다. 자세한 내용은 [키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 대화형 비디오 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

대화형 비디오 뷰어는 호스팅 페이지에 포함됩니다. 이러한 웹 페이지에는 정적 레이아웃이 있거나 &quot;응답형&quot;일 수 있으며 다른 장치 또는 다른 브라우저 창 크기에 대해 다르게 표시될 수 있습니다.

이러한 요구 사항에 맞게 뷰어는 두 가지 기본 작업 모드를 지원합니다. 고정 크기 포함 및 응답형 포함.

**고정 크기 포함 모드 및 응답형 디자인 포함 모드 정보**

포함된 모드에서 뷰어가 기존 웹 페이지에 추가되며, 이 페이지에 이미 뷰어와 관련이 없는 일부 고객 콘텐츠가 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지의 부동산의 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치를 위한 웹 페이지 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 응답형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 고정 크기 포함이 사용됩니다. 이 기능은 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

응답형 디자인 임베딩에서는 컨테이너의 크기 변경에 응답하여 뷰어가 런타임 시 크기를 조정해야 한다고 가정합니다 `DIV`. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

응답형 디자인 포함 모드에서 뷰어는 웹 페이지의 컨테이너 크기 조절 방법에 따라 다르게 동작합니다 `DIV`. 웹 페이지에서 컨테이너 너비만 설정하는 경우 `DIV`키를 제한 상태로 두면 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능을 사용하면 측면에 패딩되지 않고 자산이 보기에 완벽하게 맞습니다. 이 사용 사례는 Bootstrap 및 Foundation과 같은 반응형 웹 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적입니다.

그렇지 않으면 웹 페이지에서 뷰어 컨테이너의 너비와 높이를 모두 설정합니다 `DIV`로 지정하는 경우 뷰어는 해당 영역만 채우고 웹 페이지 레이아웃이 제공하는 크기를 따릅니다. 좋은 예는 뷰어를 모달 오버레이에 포함하는데, 이 오버레이는 웹 브라우저 창 크기에 따라 크기가 조정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 정의 `DIV`.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 다음을 포함해야 합니다 [!DNL InterativeVideoViewer.js]. 다음 [!DNL InteractiveVideoViewer.js] 파일은 [!DNL html5/js/] 표준 IS-Viewers 배포의 하위 폴더:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>기본 뷰어 JavaScript만 참조합니다 `include` 파일을 페이지에 넣을 수 있습니다. 런타임 시 뷰어의 논리에 의해 다운로드될 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조하지 마십시오. 특히 HTML5 SDK를 직접 참조하지 마십시오 `Utils.js` 뷰어에서 로드한 라이브러리 `/s7viewers` 컨텍스트 경로(소위 통합 SDK) `include`). 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리는 뷰어 논리와 뷰어 릴리스 간의 위치 변경으로 완전히 관리됩니다. Adobe은 이전 버전의 보조 뷰어를 유지하지 않습니다 `includes` 를 클릭합니다.
>
>
>따라서 보조 JavaScript에 대한 직접 참조를 보냅니다 `include` 페이지에서 뷰어에서 사용하는 는 새 제품 버전을 배포할 때 나중에 뷰어 기능을 중단합니다.

1. 컨테이너 정의 `DIV`.

   빈 항목 추가 `DIV` 뷰어를 표시할 페이지에 요소를 추가합니다. 다음 `DIV` 이 ID는 나중에 뷰어 API로 전달되므로 요소에는 해당 ID가 정의되어 있어야 합니다. DIV의 크기는 CSS를 통해 지정됩니다.

   자리 표시자 `DIV` 는 위치된 요소로서, `position` CSS 속성이 `relative` 또는 `absolute`.

   전체 화면 기능이 Internet Explorer에서 제대로 작동하려면 DOM에 자리 표시자보다 높은 스태킹 순서가 있는 다른 요소가 없는지 확인합니다 `DIV`.

   다음은 정의된 자리 표시자의 예입니다 `DIV` 요소:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 뷰어 크기 설정

   뷰어에 대한 정적 크기를 `.s7interactivevideoviewer` 절대 단위의 최상위 CSS 클래스 또는 `stagesize` 수정자.

   HTML 페이지에서 직접 CSS로 크기 조정을 지정할 수 있습니다. 또는 사용자 지정 뷰어 CSS 파일에 배치할 수 있습니다. 이 파일은 나중에 Adobe Experience Manager Assets - On-Demand의 뷰어 사전 설정 레코드에 할당되거나 를 사용하여 명시적으로 전달됩니다 `style` 명령.

   자세한 내용은 [대화형 비디오 뷰어 사용자 지정](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) css를 사용하여 뷰어 스타일을 지정하는 방법에 대한 자세한 정보.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   을(를) 설정할 수 있습니다 `stagesize` Experience Manager Assets - On-demand의 뷰어 사전 설정 레코드에 있는 수정자. 또는 다음을 사용하여 뷰어 초기화 코드로 명시적으로 전달할 수 있습니다. `params` 명령 참조 섹션에 설명된 대로 컬렉션 또는 API 호출로서 사용할 수 있습니다.

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   CSS 기반 접근 방식이 권장되며 이 예에서 사용됩니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 의 인스턴스를 만듭니다 `s7viewers.InteractiveVideoViewer` 클래스, 모든 구성 정보를 해당 생성자에 전달하고 호출 `init()` 뷰어 인스턴스의 메서드입니다. 구성 정보는 JSON 개체로 생성자에게 전달됩니다. 최소한 이 개체에는 `containerId` 뷰어 컨테이너 ID와 중첩된 이름이 들어 있는 필드 `params` 뷰어에서 지원하는 구성 매개 변수가 있는 JSON 개체.

   이 경우 `params` 개체에는 적어도 다음 방법으로 전달된 이미지 제공 URL이 있어야 합니다. `serverUrl` 속성 및 초기 자산 `asset` 매개 변수. JSON 기반 초기화 API를 사용하면 다음과 같이 전달된 비디오 서버 URL인 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다 `videoserverurl` 속성, 초기 자산 `asset` 매개 변수 및 대화형 데이터를 `interactivedata` 속성을 사용합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 DOM에 뷰어 컨테이너를 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 `init()` 닫기 바로 전 메서드 `BODY` 태그 또는 본문 `onload()` 이벤트.

   동시에 컨테이너 요소가 아직 웹 페이지 레이아웃의 일부일 필요는 없습니다. 예를 들어 `display:none` 지정된 스타일입니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 지연합니다. 이렇게 되면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에게 전달하여 생성자를 호출하는 예제입니다 `init()` 메서드를 사용합니다. 이 예제에서는 다음을 가정합니다.

   * 뷰어 인스턴스는 `interactiveVideoViewer`.
   * 자리 표시자 이름 `DIV` is `s7viewer`.
   * 이미지 제공 URL은 `https://aodmarketingna.assetsadobe.com/is/image/`.
   * 비디오 서버 URL은 `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * 콘텐츠 URL은 `https://aodmarketingna.assetsadobe.com/`.
   * 자산이 `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * 대화형 데이터는 다음과 같습니다 `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```html {.line-numbers}
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

   ```html {.line-numbers}
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

**제한 없는 높이를 사용한 반응형 디자인 포함**

반응형 디자인 포함 기능을 사용하면 일반적으로 웹 페이지에는 뷰어 컨테이너의 런타임 크기를 지시하는 유연한 레이아웃이 있습니다 `DIV`. 다음 예에서는 웹 페이지에서 뷰어의 컨테이너를 허용한다고 가정합니다 `DIV` 웹 브라우저 창 크기의 40%를 사용하고 높이는 제한이 없습니다. 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 포함 단계와 비슷합니다. 유일한 차이점은 뷰어 크기를 명시적으로 정의할 필요가 없다는 것입니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 DIV를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 포함과 동일합니다. 기존 컨테이너에 컨테이너 DIV 추가 `"holder"` DIV. 다음 코드는 완전한 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되는지 및 뷰어 종횡비가 자산과 어떻게 일치하는지 확인합니다.

```html {.line-numbers}
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

다음 예제 페이지에서는 제한 높이가 있는 반응형 디자인 포함의 실제 사용을 보여 줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[대체 데모 위치](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**너비와 높이가 정의된 응답형 포함**

너비와 높이가 정의된 응답형 임베드가 있는 경우 웹 페이지 스타일링이 다릅니다. 이 서비스는 두 가지 크기를 `"holder"` DIV를 실행하고 브라우저 창에 정렬합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소를 100%로 추가합니다.

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

나머지 포함 단계는 제한 높이가 없는 응답형 포함에 사용되는 단계와 동일합니다. 결과 예는 다음과 같습니다.

```html {.line-numbers}
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

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 이 API 생성자를 사용하면 매개 변수를 사용하지 않으며 `setContainerId()`, `setParam()`, 및 `setAsset()` 별도의 JavaScript 호출을 사용하는 API 메서드.

다음 예에서는 setter 기반 API와 함께 고정 크기 포함 사용을 보여 줍니다.

```html {.line-numbers}
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
