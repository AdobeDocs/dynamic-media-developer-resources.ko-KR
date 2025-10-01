---
title: 파노라마 뷰어
description: HTML5 Panoramic Viewer는 파노라마 이미지를 표시하는 이미지 뷰어입니다. 이 뷰어의 목적은, 등장방형적 이미지로도 알려진 구형의 파노라마를 디스플레이하는 것이다. 회전식 움직임에 의한 자동 패닝과 패닝을 지원한다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다. 가상 현실 뷰잉 모드는 지원되는 모바일 디바이스에서 이용 가능하다.
keywords: 반응형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '1920'
ht-degree: 0%

---

# 파노라마{#panoramic}

HTML5 Panoramic Viewer는 파노라마 이미지를 표시하는 이미지 뷰어입니다. 이 뷰어의 목적은, 등장방형적 이미지로도 알려진 구형의 파노라마를 디스플레이하는 것이다. 회전식 움직임에 의한 자동 패닝과 패닝을 지원한다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다. 가상 현실 뷰잉 모드는 지원되는 모바일 디바이스에서 이용 가능하다.

[시스템 요구 사항 및 필수 구성 요소](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)를 참조하십시오.


뷰어 유형 514.

<!--
## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)
-->

## 파노라마 뷰어 사용 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramic Viewer는 런타임 시 뷰어가 다운로드한 기본 JavaScript 파일과 도우미 파일 세트를 나타냅니다. 도우미 파일 세트는 이 특정 뷰어, 에셋, CSS에서 사용하는 모든 HTML5 뷰어 SDK 구성 요소에 포함된 단일 JavaScript입니다.
HTML5 Panoramic Viewer는 IS-Viewer와 함께 제공되는 프로덕션 준비 HTML 페이지를 사용하는 팝업 모드와 문서화된 API를 사용하여 대상 웹 페이지에 통합된 내장 모드 모두에서 사용할 수 있습니다.
구성 및 스키닝은 다른 HTML5 시청자의 스키닝과 유사합니다. 모든 스키닝은 맞춤형 CSS를 통해 달성할 수 있습니다.

[모든 뷰어에 공통되는 명령 참조 - 구성 특성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)을 참조하십시오.

## HTML5 Panoramic Viewer와 상호 작용 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panoramic Viewer는 드래그 또는 자이로스코프 이동을 통한 자동 패닝 및 탐색을 지원합니다.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>탐색 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>데스크톱 </p> </td> 
   <td colname="col2"> <p>탐색하려면 자동으로 패닝하고 드래그합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>터치 장치 </p> </td> 
   <td colname="col2"> <p>기본적으로 탐색하려면 자동 팬 및 끌기. VR 렌더링 모드에서 자이로스코프 이동을 사용하여 탐색합니다(vrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

뷰어는 터치 스크린 및 마우스로 Windows 장치에서 터치 입력 및 마우스 입력을 모두 지원하지만 Chrome, Internet Explorer 11 및 Edge 웹 브라우저로만 지원됩니다.
파노라마 뷰어는 vrender 수정자를 지정하여 VR(가상 현실) 모드에서 파노라마 이미지를 렌더링할 수 있습니다. Vrender가 활성화되면 파노라마 이미지가 분할 화면에 표시됩니다. 일반적인 사용 사례는 가상 현실 헤드셋에 장착된 휴대폰에 이미지를 서비스하여, 각각의 눈에 대해 별개의 이미지들을 제공하는 것일 것이다. 시청자는 머리의 회전식 움직임에 반응하여 이미지를 통해 탐색한다.

## HTML5 Panoramic Viewer 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 동작에 대한 요구 사항이 다릅니다. 경우에 따라 웹 페이지에서 링크를 제공합니다. 해당 링크를 선택하면 뷰어가 별도의 브라우저 창에서 열립니다. 다른 경우에는 호스팅 페이지에 뷰어를 임베드해야 할 수도 있습니다. 후자의 경우, 웹 페이지는 정적 레이아웃을 갖거나 &quot;응답형&quot;일 수 있으며 디바이스마다 또는 브라우저 창 크기마다 다르게 표시됩니다. 이러한 요구를 수용하기 위해 뷰어는 팝업, 고정 크기 임베딩 및 응답형 임베딩의 세 가지 기본 작업 모드를 지원합니다.

**팝업 모드 정보**

팝업 모드에서는 뷰어가 별도의 웹 브라우저 창이나 탭에서 열립니다. 브라우저 크기가 조정되거나 디바이스 방향이 변경되는 경우 전체 브라우저 창 영역을 가져와서 조정합니다.

이 모드는 모바일 장치에서 가장 일반적입니다. 웹 페이지는 `window.open()` JavaScript 호출, 올바르게 구성된 HTML 요소 또는 기타 적절한 방법을 사용하여 뷰어를 로드합니다.

팝업 작업 모드에는 기본 제공 HTML 페이지를 사용하는 것이 좋습니다. [!DNL PanoramicViewer.html]이라고 하며 표준 IS-Viewers 배포의 [!DNL html5/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

사용자 지정 CSS를 적용하여 시각적 사용자 지정을 수행할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**고정 크기 포함 모드 및 응답형 포함 모드 정보**

임베드된 모드에서는 뷰어가 기존 웹 페이지에 추가되며, 이 페이지에는 뷰어와 관련이 없는 고객 콘텐츠가 이미 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지 부동산의 일부만 점유한다.

주요 사용 사례는 데스크탑 또는 태블릿 장치 중심의 웹 페이지와 장치 유형에 따라 레이아웃을 자동으로 조정하는 응답형 웹 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않으면 고정 크기 포함이 사용됩니다. 이 방법은 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 포함은 뷰어가 컨테이너 DIV의 크기 변화에 반응하여 런타임에 크기를 조정해야 한다고 가정합니다. 가장 일반적인 사용 사례는 유연한 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

반응형 모드에서 뷰어는 웹 페이지의 컨테이너 DIV 크기 조절 방식에 따라 다르게 동작합니다. 웹 페이지에서 컨테이너 DIV의 폭만 설정하고 높이는 제한되지 않은 경우 뷰어는 사용된 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 방법을 사용하면 측면에 패딩이 없이 에셋이 보기에 완벽하게 맞습니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적입니다.

그렇지 않으면 웹 페이지에서 뷰어의 컨테이너 DIV에 대한 너비와 높이를 모두 설정하는 경우 뷰어가 해당 영역을 채우고 웹 페이지 레이아웃에서 제공하는 크기를 따릅니다. 좋은 예는 뷰어를 모달 오버레이에 포함하고, 여기서 오버레이의 크기는 웹 브라우저 창 크기에 따라 지정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. `DIV` 컨테이너를 정의하는 중입니다.
1. 뷰어 크기를 설정하는 중입니다.
1. 뷰어를 만들고 초기화하는 중입니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 [!DNL PanoramicViewer.js]을(를) 포함해야 합니다. [!DNL PanoramicViewer.js] 파일은 표준 IS-Viewers 배포의 [!DNL html5/js/] 하위 폴더에 있습니다.

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewer가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>페이지의 기본 뷰어 JavaScript `include` 파일만 참조합니다. 런타임 시 뷰어의 논리로 다운로드할 수 있는 웹 페이지 코드에 있는 추가 JavaScript 파일을 참조하지 마십시오. 특히 `Utils.js` 컨텍스트 경로의 뷰어가 로드한 HTML5 SDK `/s7viewers` 라이브러리(이른바 통합 SDK `include`)를 직접 참조하지 마십시오. 그 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리의 위치가 뷰어의 논리에 의해 완전히 관리되고 뷰어 릴리스 간 위치가 변경되기 때문입니다. Adobe은 서버에 이전 버전의 보조 뷰어 `includes`을(를) 보관하지 않습니다.
>
>
>따라서 뷰어가 사용하는 보조 JavaScript `include`을(를) 페이지에서 직접 참조하면 나중에 새 제품 버전을 배포할 때 뷰어 기능이 중단됩니다.

1. 컨테이너 DIV 정의.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. DIV 요소의 ID는 나중에 뷰어 API로 전달되므로 이 ID가 정의되어 있어야 합니다. DIV는 CSS를 통해 지정된 크기가 있습니다.

   자리 표시자 DIV는 위치 요소입니다. 즉 `position` CSS 속성이 `relative` 또는 `absolute`(으)로 설정되어 있습니다.


   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 뷰어 크기 설정

   `.s7panoramicviewer` 최상위 CSS 클래스에 대해 절대 단위로 선언하거나 `stagesize` 한정자를 사용하여 뷰어의 정적 크기를 설정할 수 있습니다.

   CSS의 크기 조절은 HTML 페이지 바로 위에 놓이거나, 나중에 AOD의 뷰어 사전 설정 레코드에 할당되거나 style 명령을 사용하여 명시적으로 전달되는 사용자 지정 뷰어 CSS 파일에 넣을 수 있습니다. CSS를 사용하여 뷰어를 스타일링하는 방법에 대한 자세한 내용은 뷰어 맞춤화 섹션을 참조하십시오. 다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` 한정자는 매개 변수 컬렉션이 있는 뷰어 초기화 코드를 사용하거나 명령 참조 섹션에 설명된 대로 API 호출로 명시적으로 전달할 수 있습니다.

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   CSS 기반 접근 방식이 권장되며 이 예제에서 사용됩니다.

1. 뷰어를 만들고 초기화하는 중입니다.

   위의 단계를 완료하면 `s7viewers.PanoramicViewer` 클래스의 인스턴스를 만들고 모든 구성 정보를 해당 생성자에 전달하고 뷰어 인스턴스에서 `init(`) 메서드를 호출합니다. 구성 정보는 JSON 개체로 생성자에 전달됩니다. 최소한 이 개체에는 뷰어에서 지원하는 구성 매개 변수와 함께 뷰어 컨테이너 ID 및 중첩된 매개 변수 JSON 개체의 이름이 들어 있는 containerId 필드가 있어야 합니다. 이 경우 params 개체에는 적어도 `serverUrl` 속성으로 전달된 이미지 제공 URL과 자산 매개 변수로 전달된 초기 자산이 있어야 합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 빌드를 지연합니다. 호환성을 최대화하려면 `init()` 태그를 닫기 직전에 또는 본문 `BODY` 이벤트에서 `onload()` 메서드를 호출하십시오.

   동시에 컨테이너 요소는 아직 웹 페이지 레이아웃의 일부가 아니어야 합니다. 예를 들어 할당된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져오는 순간까지 초기화 프로세스를 지연합니다. 이 작업이 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에 전달하고 `init()` 메서드를 호출하는 예입니다. 이 예제에서는 `panoramicViewer`이(가) 뷰어 인스턴스이고, `s7viewer`이(가) 자리 표시자 `DIV`의 이름이고, [!DNL http://s7d1.scene7.com/is/image/]이(가) 이미지 제공 URL이고, [!DNL Scene7SharedAssets/PanoramicImage-Sample]이(가) 자산이라고 가정합니다.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   다음 코드는 고정된 크기로 Panoramic Viewer를 임베드하는 간단한 웹 페이지의 전체 예입니다.

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**무제한 높이의 응답형 디자인 포함**

응답형 임베딩을 사용하면 일반적으로 웹 페이지에는 뷰어의 컨테이너 DIV의 런타임 크기를 지정하는 일종의 유연한 레이아웃이 있습니다. 이 예제의 목적상 웹 페이지를 통해 뷰어의 컨테이너 DIV가 웹 브라우저 창 크기의 80%를 차지하고 그 높이는 제한되지 않는다고 가정해 보겠습니다. 웹 페이지 HTML 코드는 다음과 같습니다.

```html {.line-numbers}
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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 포함과 유사하지만, 뷰어 크기를 명시적으로 정의할 필요가 없는 유일한 차이점이 있습니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 DIV 정의.
1. 뷰어를 만들고 초기화하는 중입니다.

위의 모든 단계는 고정 크기 포함과 동일합니다. 컨테이너 DIV를 기존 &quot;홀더&quot; DIV에 추가해야 합니다. 다음 코드는 완전한 예이며, 브라우저의 크기가 변경될 때 뷰어 크기가 어떻게 변경되고 뷰어 종횡비가 어떻게 에셋과 일치하는지 확인할 수 있습니다.

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

다음 예제 페이지는 무제한 높이로 구현된 응답형 디자인의 실제 사용을 보여 줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[대체 데모 위치](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**너비 및 높이가 정의된 응답형 디자인 포함**

너비와 높이가 정의된 응답형 디자인 임베드가 있는 경우 웹 페이지 스타일이 다릅니다. 두 크기를 &quot; 홀더&quot; `DIV`에 제공하고 브라우저 창에서 가운데로 맞춥니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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

나머지 임베딩 단계는 제한되지 않은 높이를 갖는 응답형 임베딩과 동일합니다. 결과 예는 입니다.

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**Setter 기반 API를 사용하여 포함**

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 해당 API를 사용하면 생성자는 매개 변수를 사용하지 않으며, 별도의 JavaScript 호출이 있는 `setContainerId()`, `setParam()` 및 `setAsset()` API 메서드를 사용하여 구성 매개 변수를 지정합니다.

다음 예제는 setter 기반 API를 사용한 고정 크기 임베딩을 보여 줍니다.

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
    width: 1024;
    height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
