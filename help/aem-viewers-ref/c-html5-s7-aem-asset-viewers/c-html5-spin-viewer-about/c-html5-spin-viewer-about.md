---
description: 스핀 뷰어는 적절한 스핀 세트를 사용하는 경우 이미지의 360도 보기 또는 다차원 보기를 제공하는 이미지 뷰어입니다. 확대/축소 및 회전 도구, 전체 화면 지원, 닫기 버튼 선택 사항이 있습니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.
keywords: 응답형
solution: Experience Manager
title: 회전
feature: Dynamic Media Classic,Viewers,SDK/API,스핀 세트
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2135'
ht-degree: 0%

---

# 회전{#spin}

스핀 뷰어는 적절한 스핀 세트를 사용하는 경우 이미지의 360도 보기 또는 다차원 보기를 제공하는 이미지 뷰어입니다. 확대/축소 및 회전 도구, 전체 화면 지원, 닫기 버튼 선택 사항이 있습니다. 데스크탑 및 모바일 장치에서 작동하도록 디자인되었습니다.

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형 503.

[시스템 요구 사항 및 사전 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)을 참조하십시오.

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## 스핀 뷰어 사용 {#section-e6c68406ecdc4de781df182bbd8088b4}

스핀 뷰어는 기본 JavaScript 파일 및 도우미 파일 세트(단일 JavaScript에는 이 특정 뷰어에서 사용하는 모든 Viewer SDK 구성 요소, 자산, CSS)가 런타임 시 뷰어에서 다운로드한 경우 포함됩니다.

스핀 뷰어는 IS-Viewer와 함께 제공되는 프로덕션 준비 HTML 페이지를 사용하는 팝업 모드 또는 포함된 모드에서 사용할 수 있으며, 이 페이지는 문서화된 API를 사용하여 대상 웹 페이지에 통합됩니다.

구성 및 스키닝은 다른 뷰어의 구성과 유사합니다. 모든 스키닝은 사용자 지정 CSS를 통해 수행할 수 있습니다.

모든 뷰어에 공통되는 [명령 참조 - 구성 속성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)를 참조하십시오.

## 스핀 뷰어와 상호 작용 {#section-642e66ca38cd4032992840ec6c0b0cd2}

스핀 뷰어는 다른 모바일 애플리케이션에서 일반적으로 사용되는 다음과 같은 터치 제스처를 지원합니다. 뷰어가 사용자의 스와이프 제스처를 처리할 수 없는 경우 이벤트를 웹 브라우저에 전달하여 기본 페이지 스크롤을 수행합니다. 이렇게 하면 뷰어가 장치 화면 영역의 대부분을 차지하는 경우에도 사용자가 페이지를 탐색할 수 있습니다.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>제스처 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>두 번 탭 </p> </td> 
   <td colname="col2"> <p> 최대 배율에 도달할 때까지 한 수준 확대합니다. 다음 두 번 탭 제스처는 뷰어를 초기 보기 상태로 재설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>핀치 </p> </td> 
   <td colname="col2"> <p>이미지를 확대하거나 축소합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>가로 밀기 또는 밀기 </p> </td> 
   <td colname="col2"> <p> 이미지가 재설정 상태인 경우 세트를 수평으로 순환합니다. </p> <p> 이미지를 확대하면 이미지를 가로로 이동합니다. 이미지가 보기 가장자리로 이동되고 스와이프가 해당 방향으로 계속 수행되면 제스처가 기본 페이지 스크롤을 수행합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세로 밀기 또는 밀기 </p> </td> 
   <td colname="col2"> <p> 이미지가 재설정 상태인 경우, 다차원 스핀 세트를 사용할 경우 세로 보기 각도가 변경됩니다. 1차원 스핀 세트에서, 또는 다차원 스핀 세트가 마지막 또는 첫 번째 축에 있는 경우, 세로 스와이프가 수직 뷰 각도를 변경하지 않도록 제스처가 기본 페이지 스크롤을 수행합니다. </p> <p> 이미지를 확대하면 이미지를 세로로 이동합니다. 이미지가 보기 가장자리로 이동되고 스와이프가 해당 방향으로 계속 수행되면 제스처가 기본 페이지 스크롤을 수행합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 뷰어는 터치스크린과 마우스를 사용하여 Windows 장치에서 터치 입력과 마우스 입력을 모두 지원합니다. 그러나 이 지원은 Chrome, Internet Explorer 11 및 Edge 웹 브라우저만 지원합니다.

이 뷰어는 키보드로 액세스할 수 있습니다.

[키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)을 참조하십시오.

## 포함 스핀 뷰어 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 동작에 대한 요구 사항이 다릅니다. 경우에 따라 웹 페이지에서 링크를 제공하는데, 이 링크를 클릭하면 별도의 브라우저 창에서 뷰어가 열립니다. 다른 경우 호스팅 페이지에 뷰어 권한을 포함해야 합니다. 후자의 경우, 웹 페이지에는 정적 페이지 레이아웃이 있거나, 서로 다른 장치 또는 서로 다른 브라우저 창 크기에 대해 다르게 표시되는 응답형 디자인을 사용할 수 있습니다. 이러한 요구 사항을 수용하기 위해 뷰어는 다음 세 가지 기본 작업 모드를 지원합니다. 팝업, 고정 크기 포함 및 반응형 디자인 포함

**팝업 모드 기본 정보**

팝업 모드에서는 뷰어가 별도의 웹 브라우저 창이나 탭에서 열립니다. 브라우저 크기가 조정되거나 모바일 장치의 방향이 변경되는 경우 전체 브라우저 창 영역을 가져와 조정됩니다.

팝업 모드는 모바일 장치에 가장 일반적입니다. 웹 페이지는 `window.open()` JavaScript 호출을 사용하여 뷰어를 로드하거나, 올바르게 구성된 `A` HTML 요소 또는 기타 적절한 메서드를 사용합니다.

팝업 작업 모드에 기본 HTML 페이지를 사용하는 것이 좋습니다. 이 경우, [!DNL SpinViewer.html] 이라고 하며, 표준 IS-Viewers 배포의 [!DNL html5/] 하위 폴더 내에 있습니다.

[!DNL <s7viewers_root>/html5/SpinViewer.html]

사용자 지정 CSS를 적용하여 시각적 사용자 지정을 수행할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**고정 크기 포함 모드 및 응답형 디자인 포함 모드 정보**

포함된 모드에서 뷰어가 기존 웹 페이지에 추가되며, 이 페이지에 이미 뷰어와 관련이 없는 일부 고객 콘텐츠가 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지의 부동산의 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치를 위한 웹 페이지 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 응답형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 고정 크기 포함이 사용됩니다. 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

응답형 디자인 임베딩에서는 뷰어가 컨테이너 `DIV`의 크기 변경에 응답하여 런타임 시 크기를 조정해야 할 수 있다고 가정합니다. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

응답형 디자인 포함 모드에서 뷰어는 웹 페이지의 컨테이너 `DIV`의 크기 조절 방식에 따라 다르게 동작합니다. 웹 페이지가 컨테이너 `DIV`의 너비만 설정하고 높이를 제한을 두지 않는 경우 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능을 사용하면 측면에 패딩되지 않고 자산이 보기에 완벽하게 맞습니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적입니다.

그렇지 않으면 웹 페이지가 뷰어의 컨테이너 `DIV`에 대한 너비와 높이를 모두 설정하면 뷰어가 해당 영역을 채우고 웹 페이지 레이아웃이 제공하는 크기를 따릅니다. 좋은 예는 뷰어를 모달 오버레이에 포함할 수 있습니다. 이 오버레이는 웹 브라우저 창 크기에 따라 크기가 조정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 스핀 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 `SpinViewer.js`를 포함해야 합니다. `SpinViewer.js` 는 표준 IS- [!DNL html5/js/] Viewers 배포의 하위 폴더 아래에 있습니다.

   `<s7viewers_root>/html5/js/SpinViewer.js`

   뷰어가 Adobe Dynamic Media 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media 서버 중 하나에 대한 전체 경로를 지정합니다.

   상대 경로는 다음과 같습니다.

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >페이지에서 기본 뷰어 JavaScript `include` 파일만 참조하면 됩니다. 런타임 시 뷰어의 논리로 다운로드할 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조해서는 안 됩니다. 특히 `/s7viewers` 컨텍스트 경로(소위 통합 SDK `include`)에서 뷰어가 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오. 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리의 위치가 뷰어의 논리에 의해 완전히 관리되고 뷰어 릴리스 간에 위치가 변경되기 때문입니다. Adobe은 이전 버전의 보조 뷰어 `includes`를 서버에 유지하지 않습니다.
   >
   >
   >따라서 페이지에서 뷰어가 사용하는 보조 JavaScript `include`에 직접 참조를 지정하면 새 제품 버전이 배포될 때 나중에 뷰어 기능이 중단됩니다.

1. 컨테이너 DIV를 정의합니다.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. 이 ID가 나중에 뷰어 API로 전달되므로 DIV 요소에는 해당 ID가 정의되어 있어야 합니다.

   자리 표시자 DIV는 배치된 요소입니다. 즉, `position` CSS 속성이 `relative` 또는 `absolute`로 설정되어 있습니다.

   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 뷰어 크기 설정

   `.s7spinviewer` 최상위 CSS 클래스에 대해 절대 단위로 선언하거나 `stagesize` 한정자를 사용하여 뷰어의 정적 크기를 설정할 수 있습니다.

   CSS의 크기 조정을 HTML 페이지나 사용자 지정 뷰어 CSS 파일에서 직접 배치할 수 있습니다. 이 파일은 나중에 Dynamic Media Classic의 뷰어 사전 설정 레코드에 할당되거나 스타일 명령을 사용하여 명시적으로 전달할 수 있습니다.

   CSS를 사용하여 뷰어의 스타일을 지정하는 방법에 대한 자세한 내용은 [스핀 뷰어 사용자 지정](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) 을 참조하십시오.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Dynamic Media Classic의 뷰어 사전 설정 레코드에서 `stagesize` 한정자를 설정하거나 `params` 컬렉션을 사용하는 뷰어 초기화 코드 또는 명령 참조 섹션에 설명된 대로 API 호출로 명시적으로 전달할 수 있습니다.

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   CSS 기반 접근 방식이 권장되며 이 예에서 사용됩니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.SpinViewer` 클래스의 인스턴스를 만들고 모든 구성 정보를 해당 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 JSON 개체로 생성자에게 전달됩니다. 최소한 이 개체에는 뷰어 컨테이너 ID의 이름을 포함하는 `containerId` 필드와 뷰어가 지원하는 구성 매개 변수를 사용하여 중첩된 `params` JSON 개체가 있습니다. 이 경우 `params` 개체의 경우 `serverUrl` 속성으로 전달된 이미지 제공 URL과 `asset` 매개 변수로서 초기 자산이 있어야 합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 DOM에 뷰어 컨테이너를 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 `BODY` 태그를 닫기 직전에 또는 body `onload()` 이벤트에서 `init()` 메서드를 호출하십시오.

   동시에 컨테이너 요소가 반드시 아직 웹 페이지 레이아웃의 일부일 필요는 없습니다. 예를 들어 지정된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 지연합니다. 이 작업이 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 뷰어 인스턴스를 만드는 예입니다. 이 예제에서는 `spinViewer`이 뷰어 인스턴스이고, `s7viewer`은 자리 표시자 `DIV`의 이름이고, [!DNL http://s7d1.scene7.com/is/image/]은 이미지 제공 URL이고, [!DNL Scene7SharedAssets/SpinSet_Sample]는 자산이라고 가정합니다.

   ```
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   다음 코드는 고정된 크기로 스핀 뷰어를 포함하는 간단한 웹 페이지의 전체 예입니다.

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**제한 없는 높이를 사용한 반응형 디자인 포함**

응답형 디자인 포함 기능을 사용할 경우, 일반적으로 웹 페이지에는 뷰어 컨테이너의 런타임 크기를 지시하는 유연한 레이아웃이 있습니다 `DIV`. 이 예제의 경우, 웹 페이지에서 뷰어의 컨테이너 `DIV`가 웹 브라우저 창 크기의 40%를 취할 수 있도록 허용하여 높이 제한을 두지 않는다고 가정해 보십시오. 결과 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 포함과 유사하며, 뷰어 크기를 명시적으로 정의할 필요가 없다는 유일한 차이가 있습니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 DIV를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 포함과 동일합니다. 컨테이너 `DIV`를 기존 &quot; 홀더&quot; `DIV`에 추가합니다. 다음 코드는 완전한 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되고 뷰어 종횡비가 자산과 어떻게 일치하는지 확인할 수 있습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

다음 예제 페이지에서는 제한 높이가 있는 반응형 디자인 포함 실제 사용 사례를 보여줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[대체 데모 위치](https://experienceleague.adobe.com/tools/vlist/vlist.html)

**폭과 높이가 정의된 유연한 크기 포함**

너비와 높이가 정의된 유연한 크기 포함의 경우 웹 페이지 스타일링이 다릅니다. 즉, 두 크기를 모두 &quot; 홀더&quot; `DIV`에 제공하고 브라우저 창에 배치합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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

나머지 포함 단계는 제한 높이가 없는 응답형 디자인 포함과 동일합니다. 결과 예는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter 기반 API를 사용하여 포함**

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 해당 API 생성자를 사용하면 매개 변수를 사용하지 않으며 구성 매개 변수는 별도의 JavaScript 호출과 함께 `setContainerId()`, `setParam()` 및 `setAsset()` API 메서드를 사용하여 지정합니다.

다음 예는 setter 기반 API가 포함된 고정 크기를 보여줍니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
