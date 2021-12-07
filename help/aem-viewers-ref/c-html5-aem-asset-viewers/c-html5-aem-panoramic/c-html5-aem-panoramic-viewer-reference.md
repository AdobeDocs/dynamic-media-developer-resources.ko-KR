---
title: 파노라마 뷰어
description: HTML5 파노라마 뷰어는 파노라마 이미지를 표시하는 이미지 뷰어입니다. 이 뷰어의 목적은 등사각형 이미지라고도 하는 구형 파노라마를 표시하는 것입니다. 그것은 자동 패닝 및 회전을 자극 운동으로 지지한다.  데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.  가상 현실 보기 모드는 지원 모바일 장치에서 사용할 수 있습니다.
keywords: 응답형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 0%

---

# 파노라마{#panoramic}

HTML5 파노라마 뷰어는 파노라마 이미지를 표시하는 이미지 뷰어입니다. 이 뷰어의 목적은 등사각형 이미지라고도 하는 구형 파노라마를 표시하는 것입니다. 그것은 자동 패닝 및 회전을 자극 운동으로 지지한다.  데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.  가상 현실 보기 모드는 지원 모바일 장치에서 사용할 수 있습니다.

자세한 내용은 [시스템 요구 사항 및 사전 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


뷰어 유형 514.

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## 파노라마 뷰어 사용 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 파노라마 뷰어는 기본 JavaScript 파일 및 런타임 시 뷰어가 다운로드한 모든 HTML5 Viewer SDK 구성 요소(이 특정 뷰어, 자산 및 CSS)에 포함된 단일 JavaScript 포함)를 나타냅니다.
HTML5 파노라마 뷰어는 IS-Viewer와 함께 제공된 프로덕션 준비 HTML 페이지를 사용하여 팝업 모드에서 또는 포함된 모드에서 둘 다 사용할 수 있으며, 이 페이지는 문서화된 API를 사용하여 target 웹 페이지에 통합됩니다.
구성 및 스키닝은 다른 HTML5 뷰어의 구성과 유사합니다. 모든 스키닝은 사용자 지정 CSS를 통해 수행할 수 있습니다.

자세한 내용은 [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## HTML5 파노라마 뷰어와 상호 작용 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 파노라마 뷰어는 드래그 또는 회전 운동으로 자동 패닝 및 탐색을 지원합니다.

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
   <td colname="col2"> <p>자동 패닝 후 드래그하여 탐색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>터치 장치 </p> </td> 
   <td colname="col2"> <p>기본적으로 탐색하려면 자동 패닝 후 드래그합니다. VR 렌더링 모드에서 회전 이동(vrender=true)으로 이동합니다.
 </p> </td> 
  </tr> 
 </tbody> 
</table>

뷰어는 터치 스크린 및 마우스를 사용하는 Windows 장치에서 터치 입력과 마우스 입력을 모두 지원하지만 Chrome, Internet Explorer 11 및 Edge 웹 브라우저만 지원합니다.
파노라마 뷰어는 vrender 수정자를 지정하여 VR(Virtual Reality) 모드에서 파노라마 이미지를 렌더링할 수 있습니다.  vrender를 사용하면 분할 화면에 파노라마 이미지가 표시됩니다.  일반적인 사용 사례는 가상 현실 헤드셋에 장착된 휴대폰에서 이미지를 제공하는 것이고, 각 눈을 위한 별도의 이미지를 제공하는 것이다.  시청자는 머리의 점경운동에 반응하여 이미지를 탐색할 것이다.

## 포함 HTML5 파노라마 뷰어 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 동작에 대한 요구 사항이 다릅니다. 경우에 따라 웹 페이지에서 링크를 제공할 수 있고, 해당 링크를 클릭하면 별도의 브라우저 창에서 뷰어가 열립니다. 다른 경우 호스팅 페이지에 뷰어 권한을 포함해야 할 수도 있습니다. 후자의 경우 웹 페이지에는 정적 레이아웃이 있거나 &quot;응답형&quot;일 수 있으며 다른 장치 또는 다른 브라우저 창 크기에 대해 다르게 표시됩니다. 이러한 요구 사항을 수용하기 위해 뷰어는 다음 세 가지 기본 작업 모드를 지원합니다. 팝업, 고정 크기 포함 및 응답형 포함.

**팝업 모드 기본 정보**

팝업 모드에서 뷰어는 별도의 웹 브라우저 창이나 탭에서 열립니다. 브라우저 크기가 조정되거나 장치 방향이 변경되는 경우 전체 브라우저 창 영역을 사용하고 조정됩니다.

이 모드는 모바일 장치에 가장 일반적입니다. 웹 페이지는 window.open() JavaScript 호출을 사용하여 뷰어를 로드하고, 올바르게 구성된 A HTML 요소나 기타 적절한 방법을 사용합니다.

팝업 작업 모드에서는 기본 HTML 페이지를 사용하는 것이 좋습니다. 라고 합니다 [!DNL PanoramicViewer.html] 그리고 그것은 아래에 있습니다 [!DNL html5/] 표준 IS-Viewers 배포의 하위 폴더:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

사용자 지정 CSS를 적용하여 시각적 사용자 지정을 달성할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**고정 크기 포함 모드 및 응답형 포함 모드 정보**

포함된 모드에서 뷰어가 기존 웹 페이지에 추가되며, 이 페이지에 이미 뷰어와 관련이 없는 일부 고객 콘텐츠가 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지 부동산의 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치를 위한 웹 페이지 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 응답형 웹 페이지입니다.

초기 로드 후 뷰어가 크기를 변경하지 않는 경우 크기 포함이 수정되었습니다. 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

응답형 임베드는 뷰어가 해당 컨테이너 DIV의 크기 변경에 응답하여 런타임 시 크기를 조정해야 할 수 있다고 가정합니다. 가장 일반적인 사용 사례는 유연한 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

응답형 모드에서 뷰어는 웹 페이지의 컨테이너 DIV의 크기를 조정하는 방식에 따라 다르게 동작합니다. 웹 페이지가 컨테이너 DIV의 너비만 설정하고 높이 제한을 두지 않는 경우 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이렇게 하면 측면에 패딩되지 않고 자산이 보기에 완벽하게 맞습니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 응답형 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적입니다.

그렇지 않으면 웹 페이지가 뷰어의 컨테이너 DIV에 대한 너비와 높이를 모두 설정하는 경우 뷰어는 해당 영역을 채우고 웹 페이지 레이아웃으로 제공된 크기를 따릅니다. 좋은 예는 뷰어를 모달 오버레이에 포함할 수 있습니다. 이 오버레이는 웹 브라우저 창 크기에 따라 크기가 조정됩니다.


**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 정의 `DIV`.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 다음을 포함해야 합니다 [!DNL PanoramicViewer.js]. 다음 [!DNL PanoramicViewer.js] 파일은 [!DNL html5/js/] 표준 IS-Viewers 배포의 하위 폴더:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>기본 뷰어 JavaScript만 참조합니다 `include` 파일을 페이지에 넣을 수 있습니다. 런타임 시 뷰어의 논리에 의해 다운로드될 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조하지 마십시오. 특히 HTML5 SDK를 직접 참조하지 마십시오 `Utils.js` 뷰어에서 로드한 라이브러리 `/s7viewers` 컨텍스트 경로(소위 통합 SDK) `include`). 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리는 뷰어 논리와 뷰어 릴리스 간의 위치 변경으로 완전히 관리됩니다. Adobe은 이전 버전의 보조 뷰어를 유지하지 않습니다 `includes` 를 클릭합니다.
>
>
>따라서 보조 JavaScript에 대한 직접 참조를 보냅니다 `include` 페이지에서 뷰어에서 사용하는 는 새 제품 버전을 배포할 때 나중에 뷰어 기능을 중단합니다.

1. 컨테이너 DIV를 정의합니다.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. 이 ID가 나중에 뷰어 API로 전달되므로 DIV 요소에는 해당 ID가 정의되어 있어야 합니다. DIV의 크기는 CSS를 통해 지정됩니다.

   자리 표시자 DIV는 위치된 요소, 즉 `position` CSS 속성이 `relative` 또는 `absolute`.


   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 뷰어 크기 설정

   뷰어에 대한 정적 크기를 `.s7panoramicviewer` 절대 단위의 최상위 CSS 클래스 또는 수정자 사용 `stagesize`.

   CSS의 크기 조절은 HTML 페이지 또는 나중에 AOD의 뷰어 사전 설정 레코드에 할당되거나 스타일 명령을 사용하여 명시적으로 전달되는 사용자 지정 뷰어 CSS 파일에 적용할 수 있습니다. CSS를 사용하여 뷰어의 스타일을 지정하는 방법에 대한 자세한 내용은 뷰어 섹션 사용자 지정 을 참조하십시오. 다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` 수정자는 다음과 같이 params 컬렉션을 사용하는 뷰어 초기화 코드 또는 명령 참조 섹션에 설명된 대로 API 호출로 명시적으로 전달할 수 있습니다.

   ```
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   CSS 기반 접근 방식이 권장되며 이 예에서 사용됩니다.


1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 의 인스턴스를 만듭니다 `s7viewers.PanoramicViewer` 클래스, 모든 구성 정보를 생성자에 전달하고 호출 `init(`) 메서드를 사용합니다. 구성 정보는 JSON 개체로 생성자에게 전달됩니다. 최소한, 이 개체에는 뷰어가 지원하는 구성 매개 변수와 함께 뷰어 컨테이너 ID 및 중첩 매개 변수 JSON 개체의 이름이 들어 있는 containerId 필드가 있어야 합니다. 이 경우 params 개체에는 적어도 로 전달된 이미지 제공 URL이 있어야 합니다 `serverUrl` 속성 및 초기 자산을 자산 매개 변수로 추가합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 DOM에 뷰어 컨테이너를 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 `init()` 닫기 바로 전 메서드 `BODY` 태그 또는 본문 `onload()` 이벤트.

   동시에 컨테이너 요소가 아직 웹 페이지 레이아웃의 일부일 필요는 없습니다. 예를 들어 `display:none` 지정된 스타일입니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 지연합니다. 이 작업이 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에게 전달하고 생성자를 호출하는 예제입니다 `init()` 메서드를 사용합니다. 이 예는 를 가정합니다 `panoramicViewer` 는 뷰어 인스턴스이고, `s7viewer` 은 자리 표시자의 이름입니다 `DIV`, [!DNL http://s7d1.scene7.com/is/image/] 는 이미지 제공 URL이고, [!DNL Scene7SharedAssets/PanoramicImage-Sample] 는 자산입니다.

   ```
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

   다음 코드는 고정된 크기로 파노라마 뷰어를 포함하는 작은 웹 페이지의 전체 예입니다.

   ```
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

**제한 없는 높이를 사용한 반응형 디자인 포함**

응답형 포함 웹 페이지에는 일반적으로 뷰어 컨테이너 DIV의 런타임 크기를 지시하는 유연한 레이아웃이 있습니다. 이 예제의 목적을 위해, 웹 페이지에서 뷰어의 컨테이너 DIV가 웹 브라우저 창 크기의 80%를 사용할 수 있으며, 높이는 제한되지 않습니다. 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정된 크기 포함과 매우 유사하며, 뷰어 크기를 명시적으로 정의할 필요가 없다는 유일한 차이점이 있습니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 DIV를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 포함과 동일합니다. 컨테이너 DIV는 기존 &quot;holder&quot; DIV에 추가해야 합니다. 다음 코드는 브라우저 크기를 조정할 때 뷰어 크기가 변경되는 방법과 뷰어 종횡비가 자산과 어떻게 일치하는지 확인하는 완전한 예입니다.

```
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

다음 예제 페이지에서는 제한 높이가 있는 반응형 디자인 포함의 실제 사용을 보여 줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[대체 데모 위치](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**폭 및 높이가 정의된 반응형 디자인 포함**

너비와 높이가 정의된 응답형 디자인이 있으면 웹 페이지 스타일이 다릅니다. &quot; 홀더&quot;에 두 크기를 모두 제공합니다. `DIV` 브라우저 창에서 가운데에 배치합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소를 100%:

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

나머지 포함 단계는 제한 높이가 없는 응답형 포함 단계와 동일합니다. 결과 예는 다음과 같습니다

```
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

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 해당 API를 사용하여 생성자는 매개 변수를 사용하지 않으며 구성 매개 변수를 `setContainerId()`, `setParam()`, 및 `setAsset()` 별도의 JavaScript 호출을 사용하는 API 메서드.

다음 예제에서는 setter 기반 API가 포함된 고정 크기를 보여 줍니다.

```
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
