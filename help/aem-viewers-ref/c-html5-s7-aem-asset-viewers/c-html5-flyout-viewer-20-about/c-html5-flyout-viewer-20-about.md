---
title: 플라이아웃
description: 플라이아웃 뷰어는 이미지 뷰어입니다. 사용자가 활성화하는 플라이아웃 보기에 확대 버전이 표시된 정적 이미지가 표시됩니다. 이 뷰어는 이미지 세트에서 작동하며 색상 견본을 사용하여 탐색합니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.
keywords: 응답형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# 플라이아웃{#flyout}

플라이아웃 뷰어는 이미지 뷰어입니다. 사용자가 활성화하는 플라이아웃 보기에 확대 버전이 표시된 정적 이미지가 표시됩니다. 이 뷰어는 이미지 세트에서 작동하며 색상 견본을 사용하여 탐색합니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형은 504입니다.

자세한 내용은 [시스템 요구 사항 및 사전 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 플라이아웃 뷰어 사용 {#section-f21ac23d3f6449ad9765588d69584772}

플라이아웃 뷰어는 기본 JavaScript 파일 및 도우미 파일 세트(단일 JavaScript에는 이 특정 뷰어에서 사용하는 모든 뷰어 SDK 구성 요소, 자산, CSS)가 런타임 시 뷰어에 의해 다운로드되는 모든 Viewer SDK 구성 요소가 포함됩니다

플라이아웃 뷰어는 포함된 사용용으로만 사용되며, 이는 문서화된 API를 사용하여 웹 페이지에 통합됨을 의미합니다. 플라이아웃 뷰어에 사용할 수 있는 프로덕션 준비 웹 페이지가 없습니다.

구성 및 스키닝은 다른 뷰어의 구성과 유사합니다. 사용자 지정 CSS를 사용하여 스키닝을 적용할 수 있습니다.

자세한 내용은 [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 플라이아웃 뷰어와 상호 작용 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

플라이아웃 뷰어는 다른 모바일 애플리케이션에서 일반적으로 사용되는 단일 터치 및 다중 터치 제스처를 지원합니다.

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
   <td colname="col2"> <p> 기본 확대/축소 수준과 보조 확대/축소 수준 사이의 플라이아웃 보기 또는 변경 사항을 활성화합니다. </p> </td> 
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

자세한 내용은 [키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 플라이아웃 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 동작에 대한 요구 사항이 다릅니다. 웹 페이지에는 정적 페이지 레이아웃이 있거나, 서로 다른 장치 또는 서로 다른 브라우저 창 크기에 대해 다르게 표시되는 응답형 디자인을 사용할 수 있습니다. 이러한 요구 사항에 맞게 뷰어는 두 가지 기본 작업 모드를 지원합니다. 고정 크기 포함 및 반응형 디자인 포함.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 크기 포함 모드가 사용됩니다. 이 선택 사항은 정적 페이지 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 포함 모드에서는 컨테이너의 크기 변경에 응답하여 런타임 중에 뷰어의 크기를 조정해야 한다고 가정합니다 `DIV`. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

플라이아웃 뷰어에서 응답형 디자인 포함 모드를 사용할 때는 를 사용하여 기본 보기 이미지에 대한 명시적 중단점을 지정해야 합니다 `imagereload` 매개 변수. 가장 좋은 방법은 웹 페이지 CSS에 따라 중단점을 뷰어 너비 중단점과 일치시키는 것입니다.

응답형 디자인 포함 모드에서 뷰어는 웹 페이지 컨테이너의 방식에 따라 다르게 동작합니다 `DIV` 의 크기는 입니다. 웹 페이지에서 컨테이너 너비만 설정하는 경우 `DIV`키를 제한 상태로 두면 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능은 측면에 패딩되지 않고 자산이 보기에 완벽하게 맞습니다. 이 특정 사용 사례는 Bootstrap 및 Foundation과 같은 반응형 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적입니다.

그렇지 않으면 웹 페이지에서 뷰어 컨테이너의 너비와 높이를 모두 설정합니다 `DIV`를 채우면 뷰어가 해당 영역만 채워지고 웹 페이지 레이아웃으로 제공된 크기를 따릅니다. 좋은 사용 사례 예제는 뷰어를 모달 오버레이에 포함하고, 이 오버레이는 웹 브라우저 창 크기에 따라 크기가 조정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 정의 `DIV`.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 다음을 포함해야 합니다 `FlyoutViewer.js`. `FlyoutViewer.js` 은 다음과 같습니다 [!DNL html5/js/] 표준 IS-Viewers 배포의 하위 폴더:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

뷰어가 Adobe Dynamic Media 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>기본 뷰어 JavaScript만 참조합니다 `include` 파일을 페이지에 넣을 수 있습니다. 런타임 시 뷰어의 논리에 의해 다운로드될 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조하지 마십시오. 특히 HTML5 SDK를 직접 참조하지 마십시오 `Utils.js` 뷰어에서 로드한 라이브러리 `/s7viewers` 컨텍스트 경로(소위 통합 SDK) `include`). 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리는 뷰어 논리와 뷰어 릴리스 간의 위치 변경으로 완전히 관리됩니다. Adobe은 이전 버전의 보조 뷰어를 유지하지 않습니다 `includes` 를 클릭합니다.
>
>
>따라서 보조 JavaScript에 대한 직접 참조를 보냅니다 `include` 페이지에서 뷰어에서 사용하는 는 새 제품 버전을 배포할 때 나중에 뷰어 기능을 중단합니다.

1. 컨테이너 DIV를 정의합니다.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. 이 ID가 나중에 뷰어 API로 전달되므로 DIV 요소에는 해당 ID가 정의되어 있어야 합니다.

   자리 표시자 DIV는 위치된 요소, 즉 `position` CSS 속성이 `relative` 또는 `absolute`.

   적절한 를 지정하는 것은 웹 페이지의 책임입니다 `z-index` 를 반환합니다. 이렇게 하면 뷰어의 플라이아웃 부분이 다른 웹 페이지 요소의 맨 위에 표시됩니다.

   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 뷰어 크기를 설정합니다.

   이 뷰어는 여러 항목 세트로 작업할 때 축소판을 표시합니다. 데스크탑 시스템에서는 기본 보기 아래에 축소판이 배치됩니다. 동시에 뷰어에서는 를 사용하여 런타임 중에 기본 자산을 교체할 수 있습니다 `setAsset()` API. 개발자는 새 자산에 항목이 하나만 있을 때 뷰어가 하단 영역에서 축소판 영역을 관리하는 방법을 제어할 수 있습니다. 외부 뷰어 크기를 그대로 유지한 다음 기본 보기에서 높이를 늘리고 축소판 영역을 점유할 수 있습니다. 또는 기본 보기 크기를 정적으로 유지하고 외부 뷰어 영역을 축소하여 웹 페이지 컨텐츠를 위로 이동한 다음 축소판에서 남은 사용 가능한 페이지 공간을 사용할 수 있습니다.

   외부 뷰어 제한을 그대로 유지하려면 `.s7flyoutviewer` 절대 단위의 최상위 CSS 클래스입니다. CSS의 크기 조절은 HTML 페이지 또는 사용자 지정 뷰어 CSS 파일에서 오른쪽에 배치하거나, 나중에 Dynamic Media Classic의 뷰어 사전 설정 레코드에 할당하거나, 스타일 명령을 사용하여 명시적으로 전달할 수 있습니다.

   자세한 내용은 [플라이아웃 뷰어 사용자 지정](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) css를 사용하여 뷰어 스타일을 지정하는 방법에 대한 자세한 정보.

   다음은 HTML 페이지에서 정적 외부 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음 샘플 페이지에서 고정된 외부 뷰어 영역이 있는 동작을 볼 수 있습니다. 세트 간에 전환할 때 외부 뷰어 크기가 변경되지 않습니다.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   기본 보기 차원을 정적으로 만들려면 내면에 대한 절대 단위로 뷰어 크기를 정의합니다 `Container` 다음을 사용하는 SDK 구성 요소 `.s7flyoutviewer .s7container` CSS 선택기. 또한 에 대해 정의된 고정 크기를 재정의해야 합니다 `.s7flyoutviewer` 기본 뷰어 CSS의 최상위 CSS 클래스 `auto`.

   다음은 내면에 대한 뷰어 크기를 정의하는 예입니다 `Container` 자산을 전환할 때 기본 보기 영역의 크기가 변경되지 않도록 SDK 구성 요소:

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

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   또한 기본 뷰어 CSS는 기본 외부 영역에 대해 고정 크기를 제공합니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 의 인스턴스를 만듭니다 `s7viewers.FlyoutViewer` 클래스, 모든 구성 정보를 생성자에 전달하고 호출 `init()` 뷰어 인스턴스의 메서드입니다. 구성 정보는 JSON 개체로 생성자에게 전달됩니다. 최소한 이 개체에는 `containerId` 뷰어 컨테이너 ID와 중첩된 이름이 들어 있는 필드 `params` 뷰어가 지원하는 구성 매개 변수가 있는 JSON 개체. 이 경우 `params` 개체에는 적어도 다음 방법으로 전달된 이미지 제공 URL이 있어야 합니다. `serverUrl` 속성 및 초기 자산 `asset` 매개 변수. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 DOM에 뷰어 컨테이너를 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 `init()` 닫기 바로 전 메서드 `BODY` 태그 또는 본문 `onload()` 이벤트.

   동시에 컨테이너 요소가 아직 웹 페이지 레이아웃의 일부일 필요는 없습니다. 예를 들어 `display:none` 지정된 스타일입니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 지연합니다. 이 작업이 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에게 전달하여 생성자를 호출하는 예제입니다 `init()` 메서드를 사용합니다. 이 예제에서는 를 가정합니다 `flyoutViewer` 는 뷰어 인스턴스입니다. `s7viewer` 은 자리 표시자의 이름입니다 `DIV`; `http://s7d1.scene7.com/is/image/` 는 이미지 제공 URL입니다. 및 `Scene7SharedAssets/ImageSet-Views-Sample` 는 자산입니다.

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

   다음 코드는 크기가 고정된 플라이아웃 뷰어를 포함하는 작은 웹 페이지의 전체 예입니다.

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

## 제한 없는 높이를 사용한 반응형 디자인 포함 {#section-056cb574713c4d07be6d07cf3c598839}

반응형 디자인 포함 기능을 사용하면 일반적으로 웹 페이지에는 뷰어 컨테이너의 런타임 크기를 지시하는 유연한 레이아웃이 있습니다 `DIV`. 다음 예에서는 웹 페이지에서 뷰어의 컨테이너를 허용한다고 가정합니다 `DIV` 웹 브라우저 창 크기의 40%를 사용하고 높이는 제한이 없습니다. 웹 페이지 HTML 코드는 다음과 같습니다.

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
1. 컨테이너 정의 `DIV`.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 다음 세 가지 예외가 포함된 고정 크기 포함과 동일합니다.

* 컨테이너 추가 `DIV` 기존 &quot;홀더&quot;에 `DIV`;
* 추가됨 `imagereload` 명시적 중단점이 있는 매개 변수
* 절대 단위를 사용하여 고정 뷰어 크기를 설정하는 대신 다음과 같이 뷰어 너비와 높이를 100%로 설정하는 CSS를 사용합니다.

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

다음 예제 페이지에서는 제한 높이가 있는 반응형 디자인 포함의 실제 사용을 보여 줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[대체 데모 위치](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 폭과 높이가 정의된 유연한 크기 포함 {#section-0a329016f9414d199039776645c693de}

너비와 높이가 정의된 유연한 크기가 있는 경우 웹 페이지 스타일링이 다릅니다. 이 서비스는 두 가지 크기를 `"holder"` DIV를 실행하고 브라우저 창에 정렬합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소를 100%로 추가합니다.

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

## Setter 기반 API를 사용하여 포함 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 이 API 생성자를 사용하면 매개 변수를 사용하지 않으며 `setContainerId()`, `setParam()`, 및 `setAsset()` 별도의 JavaScript 호출을 사용하는 API 메서드.

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
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```
