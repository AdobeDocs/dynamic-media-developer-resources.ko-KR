---
description: Carousel Viewer는 클릭 가능한 핫스팟 또는 영역이 있는 확대/축소할 수 없는 배너 이미지의 Carousel을 표시하는 뷰어입니다. 이 뷰어의 목적은 사용자가 배너 이미지 위에 있는 핫스팟 또는 영역을 선택하고 고객의 웹 사이트에서 Quickview 또는 제품 세부 사항 페이지로 리디렉션할 수 있는 "쇼퍼블 슬라이드" 경험을 구현하는 것입니다. 데스크탑과 모바일 디바이스에서 작동하도록 설계되었습니다.
solution: Experience Manager
title: 회전식
feature: Dynamic Media Classic,뷰어,SDK/API,회전판 배너
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1921'
ht-degree: 0%

---


# 회전식{#carousel}

Carousel Viewer는 클릭 가능한 핫스팟 또는 영역이 있는 확대/축소할 수 없는 배너 이미지의 Carousel을 표시하는 뷰어입니다. 이 뷰어의 목적은 사용자가 배너 이미지 위에 있는 핫스팟 또는 영역을 선택하고 고객의 웹 사이트에서 Quickview 또는 제품 세부 사항 페이지로 리디렉션할 수 있는 &quot;쇼퍼블 슬라이드&quot; 경험을 구현하는 것입니다. 데스크탑과 모바일 디바이스에서 작동하도록 설계되었습니다.

>[!NOTE]
>
>이미지 렌더링 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형은 511입니다.

## 데모 URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html)

## 시스템 요구 사항 {#section-b7270cc4290043399681dc504f043609}

[시스템 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)을 참조하십시오.

## 회전판 뷰어 사용 {#section-e6c68406ecdc4de781df182bbd8088b4}

Carousel Viewer는 뷰어가 런타임 시 다운로드한 기본 JavaScript 파일 및 도우미 파일 집합(단일 JavaScript에 이 특정 뷰어에서 사용하는 모든 뷰어 SDK 구성 요소, 자산, CSS)을 나타냅니다.

Carousel Viewer는 IS Viewers와 함께 제공된 프로덕션 준비 HTML 페이지를 사용하는 팝업 모드 또는 문서화된 API를 사용하여 대상 웹 페이지에 통합되는 임베디드 모드에서 모두 사용할 수 있습니다.

구성 및 스키닝은 이 도움말에 설명된 다른 뷰어와 유사합니다. 모든 스키닝은 사용자 지정 CSS를 통해 수행됩니다.

모든 뷰어에 공통되는 [명령 참조 - 모든 뷰어에 공통되는 구성 특성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 회전판 뷰어와 상호 작용 {#section-642e66ca38cd4032992840ec6c0b0cd2}

캐러셀 세트를 탐색하는 작업은 기본 보기 위로 가로 스와이프하거나 데스크톱 장치에서 사용할 수 있는 두 개의 화살표 단추를 사용하여 수행됩니다. 세트 점에는 세트 내의 현재 위치가 표시됩니다.

뷰어는 제품의 대화형 영역을 나타내기 위해 배너 이미지 상단에 핫스팟이나 영역을 렌더링할 수 있습니다.

핫스팟 또는 영역을 클릭하거나 탭하면 작성자 시간 동안 해당 핫스팟과 연관된 작업이 트리거됩니다. 작업은 웹 사이트의 다른 페이지로 리디렉션되거나, 제품 정보를 웹 페이지 로직으로 다시 전달할 수 있으며, 이를 통해 관련 제품 컨텐츠가 포함된 빠른 보기를 트리거할 수 있습니다.

뷰어는 키보드로 완벽하게 액세스할 수 있습니다.

[키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)을 참조하십시오.

## 회전판 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

**팝업 모드 정보**

팝업 모드에서 뷰어는 별도의 웹 브라우저 창이나 탭에서 열립니다. 브라우저 크기가 조정되거나 모바일 장치의 방향이 변경될 때 브라우저 창 전체 영역이 표시되고 조정됩니다.

팝업 모드는 모바일 장치에서 가장 일반적으로 사용됩니다. 웹 페이지는 `window.open()` JavaScript 호출, 적절히 구성된 `A` HTML 요소 또는 기타 적절한 방법을 사용하여 뷰어를 로드합니다.

팝업 작업 모드에 기본 HTML 페이지를 사용하는 것이 좋습니다. 이 경우 이 이름은 `CarouselViewer.html`이며 표준 IS-Viewers 배포의 `html5/` 하위 폴더 내에 있습니다.

`<s7viewers_root>/html5/CarouselViewer.html`

사용자 지정 CSS를 적용하여 시각적 사용자 지정을 실현할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**고정 크기 포함 모드 및 반응형 디자인 포함 모드 정보**

포함된 모드에서 뷰어는 기존 웹 페이지에 추가됩니다. 이 웹 페이지에는 이미 뷰어와 관련이 없는 일부 고객 콘텐츠가 있을 수 있습니다. 뷰어는 보통 웹 페이지의 부동산 중 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치의 웹 페이지 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 반응형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 크기 임베딩이 사용됩니다. 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 임베드는 뷰어의 컨테이너 `DIV`의 크기 변경에 응답하여 런타임에 뷰어 크기를 조정해야 할 수 있다고 가정합니다. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

반응형 디자인 임베드 모드에서 뷰어는 웹 페이지의 컨테이너 크기 `DIV`에 따라 다르게 동작합니다. 웹 페이지가 `DIV` 컨테이너의 너비만 설정하고 높이를 제한하지 않은 경우 뷰어는 사용된 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능을 사용하면 측면 패딩 없이 에셋이 보기에 완벽하게 맞춰집니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 웹 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적으로 사용됩니다.

그렇지 않은 경우 웹 페이지가 뷰어의 컨테이너 `DIV`에 대한 폭과 높이를 모두 설정하는 경우 뷰어는 해당 영역만 채웁니다. 또한 웹 페이지 레이아웃이 제공하는 크기를 따릅니다. 예를 들어 뷰어를 모달 오버레이에 포함시켜 오버레이의 크기가 웹 브라우저 창 크기에 따라 조정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 [!DNL CarouselViewer.js]을(를) 포함해야 합니다. [!DNL CarouselViewer.js] 파일은 표준 IS-Viewers 배포의 [!DNL html5/js/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>페이지에서 기본 뷰어 JavaScript `include` 파일만 참조하면 됩니다. 런타임에서 뷰어의 논리로 다운로드할 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조해서는 안 됩니다. 특히, 뷰어가 `/s7viewers` 컨텍스트 경로(소위 통합 SDK `include`)에서 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오. 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리의 위치가 뷰어의 논리로 완전히 관리되고 뷰어 릴리스 간에 위치가 변경되기 때문입니다. Adobe은 이전 버전의 보조 뷰어 `includes` 버전을 서버에 유지하지 않습니다.
>
>
>따라서 페이지 뷰어에서 사용하는 보조 JavaScript `include`에 직접 참조하면 새 제품 버전이 배포될 때 향후 뷰어 기능이 중단됩니다.

1. `DIV` 컨테이너를 정의합니다.

   뷰어를 표시할 페이지에 빈 `DIV` 요소를 추가합니다. 이 ID는 나중에 뷰어 API로 전달되므로 `DIV` 요소의 ID가 정의되어 있어야 합니다. DIV의 크기는 CSS를 통해 지정됩니다.

   자리 표시자 `DIV`은(는) 배치된 요소입니다. 즉, `position` CSS 속성이 `relative` 또는 `absolute`으로 설정되어 있습니다.

   다음은 정의된 자리 표시자 `DIV` 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 뷰어 크기 설정

   `.s7carouselviewer` 최상위 CSS 클래스에 대해 절대 단위로 선언하거나 `stagesize` 수정자를 사용하여 뷰어의 정적 크기를 설정할 수 있습니다.

   CSS 크기를 HTML 페이지 또는 사용자 정의 뷰어 CSS 파일에서 직접 조정할 수 있습니다. 이 CSS는 나중에 AEM Assets의 뷰어 사전 설정 레코드에 지정되거나, 요청 시 할당되거나, `style` 명령을 사용하여 명시적으로 전달됩니다.

   CSS를 사용하여 뷰어의 스타일 지정에 대한 자세한 내용은 [캐러셀 뷰어 사용자 정의](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)를 참조하십시오.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   다음과 같이 `stagesize` 수정자를 뷰어 초기화 코드로 `params` 컬렉션 또는 명령 참조 섹션에 설명된 API 호출로 명시적으로 전달할 수 있습니다.

   ```
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   CSS 기반 접근 방식이 권장되며 이 예에서 사용됩니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.CarouselViewer` 클래스의 인스턴스를 만들고 모든 구성 정보를 해당 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 생성자에게 JSON 개체로 전달됩니다. 적어도 이 개체에는 뷰어에서 지원하는 구성 매개 변수를 사용하여 뷰어 컨테이너 ID의 이름을 유지하고 중첩된 `params` JSON 개체가 있는 `containerId` 필드가 있어야 합니다. 이 경우 `params` 개체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL 이상이 있어야 하며 초기 에셋은 `asset` 매개 변수로 있어야 합니다. JSON 기반 초기화 API를 사용하여 단일 코드 행을 사용하여 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 최대 호환성을 위해 닫는 `BODY` 태그 바로 앞 또는 본문 `onload()` 이벤트에서 `init()` 메서드를 호출합니다.

   이와 동시에 컨테이너 요소가 웹 페이지 레이아웃에 반드시 포함되어야 하는 것은 아닙니다. 예를 들어, 지정된 `display:none` 스타일을 사용하여 숨겨질 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 지연합니다. 이 경우 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 예제입니다. 이 예제에서는 `carouselViewer`이(가) 뷰어 인스턴스라고 가정합니다.`s7viewer`은 자리 표시자 `DIV`;의 이름입니다.`https://adobedemo62-h.assetsadobe.com/is/image`은(는) 이미지 제공 URL이고 `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner`은(는) 자산입니다.

   ```
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   다음 코드는 고정된 크기로 회전식 뷰어를 포함하는 간단한 웹 페이지의 완벽한 예입니다.

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**제한 없는 높이를 갖는 반응형 디자인 임베드**

반응형 디자인 임베딩을 사용하면 일반적으로 웹 페이지에는 뷰어의 컨테이너 `DIV`의 런타임 크기를 지정하는 유연한 레이아웃이 있습니다. 다음 예를 들어 웹 페이지에서 뷰어의 컨테이너 `DIV`에 웹 브라우저 창 크기의 40%를 사용할 수 있다고 가정합니다. 그리고, 그것의 높이는 제한이 없다. 웹 페이지 HTML 코드는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 80%; 
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
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 임베딩과 동일합니다. 기존 `"holder"` `DIV`에 `DIV` 컨테이너를 추가합니다. 다음 코드는 완전한 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되고 뷰어 종횡비가 에셋과 어떻게 일치하는지 확인합니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

다음 예제 페이지에서는 제한이 없는 반응형 디자인 임베딩의 실제 사용을 보여줍니다.

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html)

**폭 및 높이가 정의된 유연한 크기 포함**

폭 및 높이가 정의된 유연한 크기를 포함하는 경우 웹 페이지 스타일이 다릅니다. 이 도구는 `"holder"` DIV에 두 크기를 모두 제공하고 브라우저 창에서 가운데에 표시합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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

나머지 포함 단계는 제한이 없는 포함 작업에 사용되는 단계와 동일합니다. 결과 예는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter 기반 API를 사용하여 포함**

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 인수 없음 생성자를 사용할 수 있습니다. 이 API 생성자를 사용해도 매개 변수와 구성 매개 변수는 별도의 JavaScript 호출을 사용하여 `setContainerId()`, `setParam()` 및 `setAsset()` API 메서드를 사용하여 지정되지 않습니다.

다음 예제에서는 setter 기반 API와 함께 고정 크기 임베드를 사용하는 방법을 보여 줍니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```

