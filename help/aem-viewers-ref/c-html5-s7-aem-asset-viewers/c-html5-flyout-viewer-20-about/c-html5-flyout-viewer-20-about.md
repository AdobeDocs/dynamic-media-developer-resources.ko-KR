---
description: 플라이아웃 뷰어는 이미지 뷰어입니다. 사용자가 활성화한 플라이아웃 보기에 표시된 확대 버전이 있는 정적 이미지가 표시됩니다. 이 뷰어는 이미지 세트와 함께 작동하며 견본을 사용하여 탐색합니다. 데스크탑과 모바일 디바이스에서 작동하도록 설계되었습니다.
keywords: responsive
seo-description: 플라이아웃 뷰어는 이미지 뷰어입니다. 사용자가 활성화한 플라이아웃 보기에 표시된 확대 버전이 있는 정적 이미지가 표시됩니다. 이 뷰어는 이미지 세트와 함께 작동하며 견본을 사용하여 탐색합니다. 데스크탑과 모바일 디바이스에서 작동하도록 설계되었습니다.
seo-title: 플라이아웃
solution: Experience Manager
title: 플라이아웃
topic: Dynamic media
uuid: 588e1baa-4165-4aec-8fbe-1a916c0f409f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 플라이아웃{#flyout}

플라이아웃 뷰어는 이미지 뷰어입니다. 사용자가 활성화한 플라이아웃 보기에 표시된 확대 버전이 있는 정적 이미지가 표시됩니다. 이 뷰어는 이미지 세트와 함께 작동하며 견본을 사용하여 탐색합니다. 데스크탑과 모바일 디바이스에서 작동하도록 설계되었습니다.

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형은 504입니다.

시스템 [요구 사항 및 전제 조건을 참조하십시오](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 플라이아웃 뷰어 사용 {#section-f21ac23d3f6449ad9765588d69584772}

플라이아웃 뷰어는 기본 JavaScript 파일 및 도우미 파일 집합(단일 JavaScript는 이 특정 뷰어에서 사용하는 모든 뷰어 SDK 구성 요소, 자산, CSS)을 런타임 시 뷰어에 의해 다운로드함

플라이아웃 뷰어는 포함된 용도로만 사용되며, 이것은 문서화된 API를 사용하여 웹 페이지에 통합됨을 의미합니다. 플라이아웃 뷰어에 사용할 수 있는 프로덕션 준비 웹 페이지가 없습니다.

구성 및 스키닝은 다른 뷰어와 유사합니다. 사용자 정의 CSS를 사용하여 스키닝을 적용할 수 있습니다.

모든 [뷰어에 공통으로 사용되는 명령 참조 - 구성 특성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어 - URL에 공통되는 명령 참조](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 플라이아웃 뷰어를 사용한 상호 작용 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

플라이아웃 뷰어는 다른 모바일 응용 프로그램에서 일반적으로 사용되는 단일 터치 및 다중 터치 제스처를 지원합니다.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>제스처 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>한 번의 탭 </p> </td> 
   <td colname="col2"> <p> 기본 및 보조 확대/축소 수준 간의 플라이아웃 보기를 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>가로 손가락 대기 또는 깜박임 </p> </td> 
   <td colname="col2"> <p> 견본 막대에서 견본 목록을 스크롤합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세로 스와이프 </p> </td> 
   <td colname="col2"> <p>제스처가 견본 영역 내에서 수행되는 경우 기본 페이지 스크롤이 수행됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

또한 뷰어는 터치 스크린과 마우스를 사용하는 Windows 장치에서 터치 입력 및 마우스 입력을 모두 지원합니다. 그러나 이러한 지원은 Chrome, Internet Explorer 11 및 Edge 웹 브라우저로만 제한됩니다.

이 뷰어는 키보드로 완벽하게 액세스할 수 있습니다.

키보드 [접근성 및 탐색을](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)참조하십시오.

## 플라이아웃 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 비헤이비어에 대한 요구 사항이 다릅니다. 웹 페이지에는 정적 페이지 레이아웃이 있을 수도 있고, 서로 다른 장치 또는 서로 다른 브라우저 창 크기에 대해 다르게 표시되는 반응형 디자인을 사용할 수도 있습니다. 이러한 요구 사항을 수용하기 위해 뷰어는 두 가지 기본 작업 모드를 지원합니다.고정 크기 임베드 및 반응형 디자인 임베드.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 크기 포함 모드가 사용됩니다. 이 선택 사항은 정적 페이지 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 임베드 모드에서는 컨테이너의 크기 변경에 응답하여 런타임 중에 뷰어의 크기를 조정해야 할 수 있다고 가정합니다 `DIV`. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

플라이아웃 뷰어와 함께 반응형 디자인 임베드 모드를 사용할 때는 `imagereload` 매개 변수를 사용하여 기본 보기 이미지에 대한 명확한 중단점을 지정해야 합니다. 웹 페이지 CSS에서 지정한 뷰어 폭 중단점과 중단점을 일치시키는 것이 좋습니다.

반응형 디자인 임베드 모드에서 뷰어는 웹 페이지의 컨테이너 크기 조절 방식에 따라 다르게 동작합니다 `DIV`. 웹 페이지가 컨테이너의 너비만 설정하고 높이를 제한을 두지 `DIV`않으면 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 즉, 측면에 패딩 없이 자산이 보기에 완벽하게 맞춰집니다. 이 특별한 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적으로 사용됩니다.

그렇지 않으면 웹 페이지가 뷰어의 컨테이너에 대한 너비와 높이를 모두 설정하는 `DIV`경우 뷰어는 해당 영역만 채우고 웹 페이지 레이아웃에서 제공하는 크기를 따릅니다. 뷰어를 모달 오버레이에 포함하여 오버레이의 크기가 웹 브라우저 창 크기에 따라 조정되는 것이 좋습니다.

**고정 크기 임베드**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. 컨테이너를 `DIV`정의합니다.
1. 뷰어 크기 설정
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 포함해야 `FlyoutViewer.js`합니다. `FlyoutViewer.js` 는 표준 IS-뷰어 배포의 다음 [!DNL html5/js/] 하위 폴더에 있습니다.

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

뷰어가 Adobe Scene7 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-뷰어가 설치된 Adobe Scene7 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>페이지에서 기본 뷰어 JavaScript `include` 파일만 참조해야 합니다. 런타임 시 뷰어의 논리로 다운로드될 수 있는 추가 JavaScript 파일을 웹 페이지 코드에서 참조해서는 안 됩니다. 특히, 컨텍스트 경로(소위 통합 SDK)에서 뷰어가 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오 `/s7viewers` `include`. 이유는 런타임 뷰어 라이브러리의 위치 `Utils.js` 또는 유사한 위치는 뷰어의 논리로 완전히 관리되고 뷰어 릴리스 간에 위치가 변경되기 때문입니다. Adobe는 이전 버전의 보조 뷰어를 서버에 보관하지 않습니다. `includes`
>
>
>따라서 페이지에서 뷰어가 `include` 사용하는 보조 JavaScript에 직접 참조를 지정하면 새 제품 버전이 배포될 때 나중에 뷰어 기능이 중단됩니다.

1. 컨테이너 DIV를 정의합니다.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. 이 ID가 나중에 뷰어 API로 전달되므로 DIV 요소에 ID가 정의되어 있어야 합니다.

   자리 표시자 DIV는 위치 요소입니다. 즉, CSS `position` 속성이 `relative` 또는 `absolute`로 설정되어 있습니다.

   자리 표시자 DIV 요소에 대한 적절한 `z-index` 값을 지정하는 것은 웹 페이지의 책임입니다. 이렇게 하면 뷰어의 플라이아웃 부분이 다른 웹 페이지 요소 위에 표시됩니다.

   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 뷰어 크기 설정

   이 뷰어는 다중 항목 세트로 작업할 때 축소판을 표시합니다. 데스크탑 시스템에서 축소판은 기본 보기 아래에 표시됩니다. 동시에 뷰어는 API를 사용하여 런타임 중에 기본 에셋을 교환하도록 `setAsset()` 허용합니다. 개발자는 새 자산에 항목이 하나만 있을 때 뷰어가 하단 영역에서 축소판 영역을 관리하는 방법을 제어할 수 있습니다. 외부 뷰어 크기를 그대로 유지하고 기본 보기를 통해 높이를 늘리고 축소판 영역을 차지할 수 있습니다. 또는 기본 보기 크기를 정적으로 유지하고 외부 뷰어 영역을 축소하여 웹 페이지 컨텐츠를 위로 이동한 다음 축소판에서 남은 무료 페이지 공간을 사용할 수 있습니다.

   외부 뷰어 경계를 그대로 유지하려면 최상위 CSS 클래스의 크기를 절대 단위로 `.s7flyoutviewer` 정의합니다. CSS의 크기 조정은 HTML 페이지 또는 나중에 Scene7 Publishing System의 뷰어 사전 설정 레코드에 할당되거나 스타일 명령을 사용하여 명시적으로 전달된 사용자 정의 뷰어 CSS 파일에서 바로 가져올 수 있습니다.

   CSS를 [사용하여](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) 뷰어의 스타일 지정에 대한 자세한 내용은 플라이아웃 뷰어 사용자 지정을 참조하십시오.

   다음은 HTML 페이지에서 정적 외부 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음 샘플 페이지에서 고정된 외부 뷰어 영역에서 동작을 볼 수 있습니다. 세트 간에 전환할 때 외부 뷰어 크기는 변경되지 않습니다.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   기본 보기 크기를 정적으로 하려면 CSS 선택기를 사용하여 내부 SDK 구성 요소의 절대 단위로 뷰어 크기를 `Container``.s7flyoutviewer .s7container` 정의합니다. 또한 기본 뷰어 CSS에서 `.s7flyoutviewer` 최상위 CSS 클래스에 대해 정의된 고정 크기를 로 설정하여 재정의해야 `auto`합니다.

   다음은 자산을 전환할 때 기본 보기 영역의 크기가 변경되지 않도록 내부 `Container` SDK 구성 요소의 뷰어 크기를 정의하는 예입니다.

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

   다음 샘플 페이지는 기본 보기 크기가 고정된 뷰어 동작을 보여줍니다. 세트 간에 전환할 때 기본 보기는 정적 상태로 유지되며 웹 페이지 컨텐츠는 세로로 이동됩니다.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   또한 기본 뷰어 CSS는 외부 영역에 대해 고정된 크기를 제공합니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.FlyoutViewer` 클래스 인스턴스를 만들고 모든 구성 정보를 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 생성자에게 JSON 개체로 전달됩니다. 최소한 이 개체에는 뷰어가 지원하는 구성 매개 변수를 사용하여 뷰어 컨테이너 ID의 이름과 중첩된 `containerId` `params` JSON 개체가 있는 필드가 있어야 합니다. 이 경우 `params` 개체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL 이상이 있어야 하며 초기 자산은 `asset` 매개 변수로 전달되어야 합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행을 사용하여 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 닫는 `init()` 태그 바로 앞 또는 body `BODY` `onload()` 이벤트에서 메서드를 호출합니다.

   동시에 컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 될 필요는 없습니다. 예를 들어, 지정된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 지연합니다. 이 경우 뷰어 부하가 자동으로 다시 시작됩니다.

   다음은 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 뷰어 인스턴스를 만드는 예입니다. 이 예제에서는 뷰어 `flyoutViewer` 인스턴스가 있다고 가정합니다.자리 표시자의 `s7viewer` 이름입니다. `DIV`;이미지 제공 `http://s7d1.scene7.com/is/image/` URL;자산이 `Scene7SharedAssets/ImageSet-Views-Sample` 다음과 같습니다.

   ```
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   다음 코드는 고정된 크기의 플라이아웃 뷰어를 포함하는 간단한 웹 페이지의 전체 예입니다.

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
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
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

## 제한 없는 높이로 반응형 디자인 임베드 {#section-056cb574713c4d07be6d07cf3c598839}

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 임베드 단계와 유사합니다. 유일한 차이는 기본 뷰어 CSS에서 크기(상대 단위)가 설정된 고정 크기를 무시해야 한다는 점입니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. 컨테이너를 `DIV`정의합니다.
1. 뷰어 크기 설정
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 다음 세 가지 예외가 있는 고정 크기 임베드와 같습니다.

* 기존 &quot;소유자&quot; `DIV` 에 컨테이너를 `DIV`추가합니다.
* 명시적 중단점이 있는 `imagereload` 매개 변수가 추가되었습니다.
* 절대 단위를 사용하여 고정 뷰어 크기를 설정하는 대신, 다음과 같이 뷰어 너비와 높이를 100%로 설정하는 CSS를 사용합니다.

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

다음 코드는 전체 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되고 뷰어 종횡비가 자산과 어떻게 일치하는지 확인합니다.

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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

다음 예제 페이지에서는 제한 없는 높이와 함께 반응형 디자인 임베딩의 실제 사용을 보여줍니다.

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## 폭 및 높이가 정의된 유연한 크기 임베드 {#section-0a329016f9414d199039776645c693de}

폭 및 높이가 정의된 유연한 크기를 포함하는 경우 웹 페이지 스타일이 다릅니다. DIV에 두 가지 크기를 `"holder"` 제공하고 브라우저 창에서 가운데에 표시합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Setter 기반 API를 사용하여 임베드 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSON 기반 초기화를 사용하는 대신 setter 기반 API와 인수 없음 생성자를 사용할 수 있습니다. 이 API 생성자를 사용하면 매개 변수를 사용하지 않으며 별도의 JavaScript 호출과 함께 `setContainerId()`API 메서드 `setParam()`및 `setAsset()` API 메서드를 사용하여 구성 매개 변수를 지정할 수 있습니다.

다음 예제에서는 setter 기반 API와 함께 고정 크기 임베드 사용을 보여 줍니다.

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
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```

