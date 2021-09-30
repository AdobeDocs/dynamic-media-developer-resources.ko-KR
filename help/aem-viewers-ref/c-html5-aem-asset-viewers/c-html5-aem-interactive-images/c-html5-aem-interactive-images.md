---
title: 대화형 이미지
description: 대화형 이미지 뷰어는 클릭 가능한 핫스팟이 있는 확장 불가능한 단일 이미지를 표시하는 뷰어입니다. 이 뷰어의 목적은 "쇼퍼블 배너" 경험을 구현하는 것입니다. 즉, 사용자는 배너 이미지 위에 핫스팟을 선택하고 웹 사이트의 Quickview 또는 제품 세부 사항 페이지로 리디렉션할 수 있습니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1720'
ht-degree: 0%

---

# 대화형 이미지{#interactive-image}

대화형 이미지 뷰어는 클릭 가능한 핫스팟이 있는 확장 불가능한 단일 이미지를 표시하는 뷰어입니다. 이 뷰어의 목적은 &quot;쇼퍼블 배너&quot; 경험을 구현하는 것입니다. 즉, 사용자는 배너 이미지 위에 핫스팟을 선택하고 웹 사이트의 Quickview 또는 제품 세부 사항 페이지로 리디렉션할 수 있습니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형은 508입니다.

## 데모 URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## 시스템 요구 사항 {#section-b7270cc4290043399681dc504f043609}

[시스템 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)을 참조하십시오.

## 대화형 이미지 뷰어 사용 {#section-e6c68406ecdc4de781df182bbd8088b4}

대화형 이미지 뷰어는 런타임 시 뷰어가 다운로드한 기본 JavaScript 파일 및 도우미 파일 세트(단일 JavaScript에는 이 특정 뷰어에서 사용하는 모든 뷰어 SDK 구성 요소, 자산, CSS)가 포함됩니다.

대화형 이미지 뷰어는 포함된 모드에서만 사용할 수 있으며, 이 모드에서는 문서화된 API를 사용하여 Target 웹 페이지에 통합됩니다.

구성 및 스키닝은 이 도움말에 설명된 다른 뷰어의 구성과 유사합니다. 모든 스키닝은 사용자 지정 CSS를 통해 수행됩니다.

모든 뷰어에 공통되는 [명령 참조 - 구성 속성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)를 참조하십시오.

## 대화형 이미지 뷰어와 상호 작용 {#section-642e66ca38cd4032992840ec6c0b0cd2}

비디오 이미지 뷰어에서 지원하는 상호 작용은 데스크탑 시스템에서 핫스팟 활성화입니다. 이 활성화는 클릭 및 터치 장치에서 한 번의 탭으로 발생합니다.

뷰어는 키보드로 액세스할 수 있습니다.

[키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)을 참조하십시오.

## 대화형 이미지 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

대화형 이미지 뷰어는 호스팅 페이지에 포함됩니다. 이러한 웹 페이지에는 정적 레이아웃이 있거나 &quot;응답형&quot;일 수 있으며 다른 장치 또는 다른 브라우저 창 크기에 대해 다르게 표시될 수 있습니다.

이러한 요구 사항에 맞게 뷰어는 두 가지 기본 작업 모드를 지원합니다. 고정 크기 포함 및 응답형 포함.

**고정 크기 포함 모드 및 응답형 디자인 포함 모드 정보**

포함된 모드에서는 뷰어가 기존 웹 페이지에 추가됩니다. 이 웹 페이지에는 이미 뷰어와 관련이 없는 일부 고객 콘텐츠가 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지의 부동산의 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치를 위한 웹 페이지 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 응답형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 고정 크기 포함이 사용됩니다. 이 방법은 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 포함 에서는 컨테이너 `DIV`의 크기 변경에 응답하여 뷰어가 런타임 시 크기를 조정해야 한다고 가정합니다. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

응답형 디자인 포함 모드에서 뷰어는 웹 페이지의 컨테이너 `DIV`의 크기 조절 방식에 따라 다르게 동작합니다. 웹 페이지가 컨테이너 `DIV`의 너비만 설정하고 높이를 제한을 두지 않는 경우 뷰어는 사용된 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능을 사용하면 측면에 패딩되지 않고 자산이 보기에 완벽하게 맞습니다. 이 사용 사례는 Bootstrap 및 Foundation과 같은 반응형 웹 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적입니다.

그렇지 않으면 웹 페이지가 뷰어의 컨테이너 `DIV`에 대한 너비와 높이를 모두 설정하면 뷰어가 해당 영역만 채웁니다. 또한 웹 페이지 레이아웃이 제공하는 크기를 따릅니다. 좋은 예는 뷰어를 모달 오버레이에 포함하는데, 이 오버레이는 웹 브라우저 창 크기에 따라 크기가 조정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 [!DNL InterativeImage.js]를 포함해야 합니다. [!DNL InteractiveImage.js] 파일은 표준 IS-Viewers 배포의 [!DNL html5/js/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Adobe Dynamic Media Classic 서버 중 하나에 뷰어가 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>페이지에서 기본 뷰어 JavaScript `include` 파일만 참조합니다. 런타임 시 뷰어의 논리에 의해 다운로드될 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조하지 마십시오. 특히 `/s7viewers` 컨텍스트 경로(소위 통합 SDK `include`)에서 뷰어가 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오. 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리의 위치가 뷰어의 논리에 의해 완전히 관리되고 뷰어 릴리스 간에 위치가 변경되기 때문입니다. Adobe은 이전 버전의 보조 뷰어 `includes`를 서버에 유지하지 않습니다.
>
>
>따라서 페이지에서 뷰어가 사용하는 보조 JavaScript `include`에 직접 참조를 지정하면 새 제품 버전이 배포될 때 나중에 뷰어 기능이 중단됩니다.

1. `DIV` 컨테이너를 정의합니다.

   뷰어를 표시할 페이지에 빈 `DIV` 요소를 추가합니다. 이 ID가 나중에 뷰어 API로 전달되므로 `DIV` 요소에는 해당 ID가 정의되어 있어야 합니다. DIV의 크기는 CSS를 통해 지정됩니다.

   자리 표시자 `DIV`는 위치하는 요소입니다. 즉, `position` CSS 속성이 `relative` 또는 `absolute`로 설정되어 있습니다.

   다음은 정의된 자리 표시자 `DIV` 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 뷰어 크기 설정

   `.s7interactiveimage` 최상위 CSS 클래스에 대해 절대 단위로 선언하거나 `stagesize` 한정자를 사용하여 뷰어의 정적 크기를 설정할 수 있습니다.

   HTML 페이지에서 직접 CSS로 크기 조정을 지정할 수 있습니다. 또는 사용자 지정 뷰어 CSS 파일에 크기 조정을 배치할 수 있습니다. 이 파일은 나중에 Adobe Experience Manager Assets - On-Demand의 뷰어 사전 설정 레코드에 할당되거나 `style` 명령을 사용하여 명시적으로 전달됩니다.

   CSS를 사용하여 뷰어의 스타일을 지정하는 방법에 대한 자세한 내용은 [비디오](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)을 참조하십시오.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   다음과 같이 명령 참조 섹션에 설명된 대로 뷰어 초기화 코드를 사용하여 `stagesize` 한정자를 명시적으로 전달하거나 API 호출로 전달할 수 있습니다.`params`

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   CSS 기반 접근 방식이 권장되며 이 예에서 사용됩니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.InteractiveImage` 클래스의 인스턴스를 만들고 모든 구성 정보를 해당 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 JSON 개체로 생성자에게 전달됩니다. 최소한 이 개체에는 뷰어 컨테이너 ID의 이름을 포함하는 `containerId` 필드가 있어야 하며, 뷰어에서 지원하는 구성 매개 변수와 함께 중첩된 `params` JSON 개체가 있어야 합니다. 이 경우 `params` 개체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL 이상이 있어야 하며 초기 자산은 `asset` 매개 변수여야 합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 DOM에 뷰어 컨테이너를 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 `BODY` 태그를 닫기 직전에 또는 body `onload()` 이벤트에서 `init()` 메서드를 호출하십시오.

   동시에 컨테이너 요소가 아직 웹 페이지 레이아웃의 일부일 필요는 없습니다. 예를 들어 지정된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 지연합니다. 이 이벤트가 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 예제입니다. 이 예제에서는 `interactiveImage`이 뷰어 인스턴스라고 가정합니다. `s7viewer` 은 자리 표시자 `DIV`;의 이름입니다. `http://aodmarketingna.assetsadobe.com/is/image`은 이미지 제공 URL이고 `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.`는 자산입니다.

   ```
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   다음 코드는 고정된 크기로 비디오 이미지 뷰어를 포함하는 간단한 웹 페이지의 전체 예입니다.

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**제한 없는 높이를 사용한 반응형 디자인 포함**

응답형 디자인 포함 기능을 사용할 경우, 일반적으로 웹 페이지에는 뷰어 컨테이너의 런타임 크기를 지시하는 유연한 레이아웃이 있습니다 `DIV`. 다음 예를 들어, 웹 페이지에서 뷰어의 컨테이너 `DIV`가 웹 브라우저 창 크기의 40%를 사용할 수 있다고 가정해 보겠습니다. 그리고, 그것의 높이는 제한 없이 남아 있습니다. 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 포함 단계와 비슷합니다. 유일한 차이점은 뷰어 크기를 명시적으로 정의할 필요가 없다는 것입니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 포함과 동일합니다. 기존 `"holder"` `DIV`에 `DIV` 컨테이너를 추가합니다. 다음 코드는 완전한 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되고 뷰어 종횡비가 자산과 어떻게 일치하는지 확인합니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

다음 예제 페이지에서는 제한 높이가 있는 반응형 디자인 포함의 실제 사용을 보여 줍니다.

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**폭 및 높이가 정의된 유연한 크기 포함**

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

나머지 포함 단계는 제한 높이가 없는 응답형 포함에 사용되는 단계와 동일합니다. 결과 예는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Setter 기반 API를 사용하여 포함**

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 이 API 생성자를 사용하면 매개 변수를 사용하지 않으며 구성 매개 변수는 별도의 JavaScript 호출과 함께 `setContainerId()`, `setParam()` 및 `setAsset()` API 메서드를 사용하여 지정합니다.

다음 예에서는 setter 기반 API와 함께 고정 크기 포함 사용을 보여 줍니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```
