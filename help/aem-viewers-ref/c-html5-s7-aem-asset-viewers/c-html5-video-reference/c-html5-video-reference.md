---
title: 비디오
description: 비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다. Dynamic Media이 포함된 Dynamic Media Classic 또는 Adobe Experience Manager에서 제공됩니다.
keywords: 반응형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2368'
ht-degree: 0%

---

# 비디오{#video}

비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다. Dynamic Media Classic 또는 Dynamic Media이 있는 Experience Manager에서 제공됩니다.

다음을 참조하십시오 [시스템 요구 사항 및 사전 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

단일 비디오와 응용 비디오 세트가 모두 지원됩니다. 또한 뷰어는 외부 위치에 호스팅된 점진적 비디오 및 HLS 스트림 작업을 지원합니다. HTML5 비디오를 지원하는 데스크탑 및 모바일 웹 브라우저에서 모두 작동하도록 설계되었습니다. 이 뷰어는 또한 비디오 콘텐츠, 비디오 챕터 탐색 및 소셜 미디어 공유 도구 위에 표시되는 선택적 폐쇄 캡션을 지원합니다.

비디오 뷰어는 기본 시스템이 지원할 때마다 기본 구성에서 HLS 형식의 HTML5 스트리밍 비디오 재생을 사용합니다. HTML5 스트리밍을 지원하지 않는 시스템에서는 뷰어가 HTML5 점진적 비디오 제공으로 대체됩니다.

뷰어 유형 506.

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## 비디오 뷰어 사용 {#section-f21ac23d3f6449ad9765588d69584772}

비디오 뷰어는 기본 JavaScript 파일 및 도우미 파일 세트를 나타냅니다. 단일 JavaScript에는 런타임 시 뷰어가 다운로드한 이 특정 뷰어, 에셋 및 CSS에서 사용하는 모든 뷰어 SDK 구성 요소가 포함되어 있습니다.

IS-Viewer와 함께 제공된 프로덕션 준비 HTML 페이지를 사용하여 팝업 모드에서 비디오 뷰어를 사용할 수 있습니다. 또는 내장된 모드로 뷰어를 사용할 수 있습니다. 이 모드에서는 문서화된 API를 사용하여 뷰어가 타겟 웹 페이지에 통합됩니다.

시청자를 구성하고 스키닝하는 작업은 다른 시청자와 유사하다. 모든 스키닝은 사용자 지정 CSS를 통해 수행됩니다.

다음을 참조하십시오 [모든 뷰어에 공통되는 명령 참조 - 구성 속성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 대해 공통되는 명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 비디오 뷰어와 상호 작용 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Video Viewer는 재생/일시 중지 단추, 비디오 스크러버 비디오 시간 버블, 재생 시간/총 시간 표시기, 볼륨 컨트롤, 전체 화면 단추 및 닫힌 캡션 전환과 같은 비디오 재생을 위한 표준 사용자 인터페이스 컨트롤 세트를 제공합니다. 이러한 모든 컨트롤은 뷰어 사용자 인터페이스 하단에 있는 컨트롤 막대로 그룹화됩니다.

터치 장치에서는 하드웨어 버튼을 통해서만 볼륨을 제어할 수 있으므로 볼륨 컨트롤이 사용자 인터페이스에 표시되지 않습니다.

뷰어가 팝업 모드로 작동되는 경우 전체 화면 버튼이 사용자 인터페이스에서 사용할 수 없습니다.

비디오 챕터가 활성화되면 비디오 콘텐츠를 빠르게 탐색할 수 있습니다. 비디오 챕터는 비디오 스크러버 트랙에 마커로 표시되며 마우스 롤오버 시 또는 터치 시스템을 한 번 탭하여 챕터 제목과 관련 설명을 표시합니다. 사용자는 챕터 마커를 선택하거나 챕터 설명 버블을 선택하여 특정 챕터를 찾을 수 있습니다.

뷰어는 터치 스크린 및 마우스로 Windows 장치에서 터치 입력 및 마우스 입력을 모두 지원합니다. 그러나 이 지원은 Chrome, Internet Explorer 11 및 Edge 웹 브라우저로만 제한됩니다.

이 뷰어는 키보드에 완전히 액세스할 수 있습니다.

다음을 참조하십시오 [키보드 접근성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 비디오 뷰어를 통한 소셜 미디어 공유 도구 {#section-907d316fe1da4b87abb9775f02464704}

비디오 뷰어는 소셜 미디어 공유 도구를 지원합니다. 이 버튼은 사용자가 클릭하거나 탭하면 공유 도구 모음으로 확장되는 사용자 인터페이스에서 단일 버튼으로 사용할 수 있습니다.

공유 도구 모음에는 Facebook, Twitter, 이메일 공유, 포함 코드 공유 및 링크 공유와 같이 지원되는 각 공유 채널 유형에 대한 아이콘이 있습니다. 이메일 공유, 포함 공유 또는 링크 공유 도구가 활성화되면 뷰어에 해당 데이터 입력 양식이 있는 모달 대화 상자가 표시됩니다. facebook 또는 Twitter이 호출되면 뷰어는 사용자를 소셜 미디어 서비스에서 표준 공유 대화 상자로 리디렉션합니다. 또한 공유 도구가 활성화되면 비디오 재생이 자동으로 일시 중지됩니다.

웹 브라우저 보안 제한으로 인해 공유 도구를 전체 화면 모드에서 사용할 수 없습니다.

## 비디오 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 동작에 대한 요구 사항이 다릅니다. 경우에 따라 웹 페이지에서 링크를 제공하여 선택하면 뷰어가 별도의 브라우저 창에서 열립니다. 다른 경우에는 뷰어를 호스팅 페이지에 직접 임베드해야 합니다. 후자의 경우, 웹 페이지는 정적 페이지 레이아웃을 갖거나, 다른 디바이스에서 또는 다른 브라우저 창 크기에 대해 다르게 표시되는 반응형 디자인을 사용할 수 있습니다. 이러한 요구를 수용하기 위해 뷰어는 팝업, 고정 크기 포함, 반응형 디자인 포함 등 세 가지 기본 작업 모드를 지원합니다.

태블릿과 모바일 장치에서 동일한 페이지에 여러 비디오를 포함할 수 있습니다. 일반적으로 한 번에 하나의 비디오만 재생할 수 있습니다. 사용자가 한 비디오를 재생하기 시작한 다음 다른 비디오를 재생하려고 하면 첫 번째 비디오가 자동으로 일시 중지됩니다. 자동 일시 중지된 비디오는 현재 재생 시간을 기억하므로 사용자는 언제든지 비디오로 돌아가 재생을 재개할 수 있습니다. 이 규칙은 Android™ 4.x 장치의 Chrome 브라우저에서 유일하게 적용되지 않으며, 동시에 비디오를 재생할 수 있습니다.

**팝업 모드 정보**

팝업 모드에서는 뷰어가 별도의 웹 브라우저 창 또는 탭에서 열립니다. 브라우저 크기가 조정되거나 디바이스 방향이 변경되는 경우 전체 브라우저 창 영역을 가져와서 조정합니다.

이 모드는 모바일 장치에서 가장 일반적입니다. 웹 페이지는 다음을 사용하여 뷰어를 로드합니다. `window.open()` JavaScript 호출, 올바르게 구성됨 `A` HTML 요소 또는 임의의 다른 적절한 방법.

팝업 작업 모드에는 기본 제공 HTML 페이지를 사용하는 것이 좋습니다. 라고 합니다. [!DNL VideoViewer.html] and it is located위치 under아래에 [!DNL html5/] 표준 IS-Viewers 배포의 하위 폴더:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

사용자 지정 CSS를 적용하여 시각적 맞춤화를 수행할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**고정 크기 포함 모드 및 응답형 포함 모드 정보**

내장 모드에서 뷰어는 기존 웹 페이지에 추가되며, 이 웹 페이지에는 뷰어와 관련이 없는 고객 콘텐츠가 이미 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지의 부동산의 일부만 점유한다.

주요 사용 사례는 데스크탑 또는 태블릿 장치 중심의 웹 페이지와 장치 유형에 따라 레이아웃을 자동으로 조정하는 응답형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않으면 고정 크기 포함이 사용됩니다. 이 선택은 정적 페이지 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 포함에서는 뷰어가 컨테이너의 크기 변화에 반응하여 런타임에 크기를 조정해야 한다고 가정합니다 `DIV`. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

반응형 디자인 포함 모드에서 뷰어는 웹 페이지의 컨테이너 크기 조절 방식에 따라 다르게 동작합니다 `DIV`. 웹 페이지에서 컨테이너의 폭만 설정하는 경우 `DIV`의 높이를 제한하지 않고, 뷰어는 사용되는 에셋의 종횡비에 따라 높이를 자동으로 선택합니다. 이 방법을 사용하면 에셋이 측면에 패딩 없이 보기에 완벽하게 맞습니다. 이 사용 사례는 Bootstrap 또는 Foundation과 같은 반응형 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적으로 사용됩니다.

그렇지 않으면 웹 페이지에서 뷰어의 컨테이너에 대한 너비와 높이를 모두 설정합니다 `DIV`, 뷰어는 해당 영역만 채우고 웹 페이지 레이아웃에서 제공하는 크기를 따릅니다. 좋은 예는 뷰어를 모달 오버레이에 포함하고, 여기서 오버레이의 크기는 웹 브라우저 창의 크기에 따라 지정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 정의 `DIV`.
1. 뷰어 크기를 설정하는 중입니다.
1. 뷰어를 만들고 초기화하는 중입니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하기 전에 다음을 포함해야 합니다. [!DNL FlyoutViewer.js]. 다음 [!DNL FlyoutViewer.js] 파일은 아래에 있습니다. [!DNL html5/js/] 표준 IS-Viewers 배포의 하위 폴더:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewer가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>기본 뷰어 JavaScript만 참조 `include` 파일을 페이지에 넣습니다. 런타임 시 뷰어의 논리로 다운로드할 수 있는 웹 페이지 코드의 추가 JavaScript 파일을 참조하지 마십시오. 특히, HTML5 SDK를 직접 참조하지 마십시오 `Utils.js` 다음에서 뷰어에 의해 로드된 라이브러리 `/s7viewers` 컨텍스트 경로(소위 통합 SDK) `include`). 이유는 이(가) `Utils.js` 또는 유사한 런타임 뷰어 라이브러리는 뷰어의 논리에 의해 완전히 관리되며 뷰어 릴리스 간 위치가 변경됩니다. Adobe이 이전 버전의 보조 뷰어를 유지하지 않음 `includes` 서버에 있습니다.
>
>
>따라서 보조 JavaScript에 직접 참조 `include` 페이지의 뷰어에서 사용하는 는 향후 새 제품 버전이 배포될 때 뷰어 기능이 중단됩니다.

1. 컨테이너 DIV 정의.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. DIV 요소의 ID는 나중에 뷰어 API로 전달되므로 이 ID가 정의되어 있어야 합니다. DIV는 CSS를 통해 지정된 크기가 있습니다.

   자리 표시자 DIV는 배치된 요소이며, 즉 `position` CSS 속성이 다음으로 설정됨 `relative` 또는 `absolute`.

   Internet Explorer에서 전체 화면 기능이 제대로 작동하는지 확인하십시오. DOM에 자리 표시자 DIV보다 높은 스택 순서가 있는 다른 요소가 없는지 확인하십시오.

   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 뷰어 크기 설정

   다음에 대해 선언하여 뷰어의 정적 크기를 설정할 수 있습니다. `.s7videoviewer` 최상위 CSS 클래스(절대 단위)를 참조하거나 수정자를 사용하여 `stagesize`.

   크기 조정을 HTML 페이지의 오른쪽 CSS 또는 사용자 지정 뷰어 CSS 파일에 넣을 수 있습니다. 이 레코드는 나중에 Dynamic Media Classic의 뷰어 사전 설정 레코드에 할당되거나 스타일 명령을 사용하여 명시적으로 전달됩니다.

   다음을 참조하십시오 [비디오 뷰어 사용자 지정](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) css를 사용하여 뷰어를 스타일링하는 방법에 대한 자세한 내용을 확인하십시오.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예제입니다.

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음을 설정할 수 있습니다. `stagesize` 수정자를 Dynamic Media Classic의 뷰어 사전 설정 레코드에 포함하거나, 다음을 사용하여 뷰어 초기화 코드로 명시적으로 전달합니다. `params` 컬렉션. 또는 다음과 같이 명령 참조 섹션에 설명된 대로 API 호출로 사용됩니다.

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   CSS 기반 접근 방식이 권장되며 이 예제에서 사용됩니다.

1. 뷰어를 만들고 초기화하는 중입니다.

   위의 단계를 완료하면 인스턴스를 `s7viewers.VideoViewer` 클래스에서 모든 구성 정보를 생성자에 전달하고 `init()` 뷰어 인스턴스의 메서드입니다. 구성 정보는 JSON 개체로 생성자에 전달됩니다. 최소한 이 개체에는 다음이 있어야 합니다. `containerId` 뷰어 컨테이너 ID의 이름과 중첩된 필드가 포함된 필드 `params` 뷰어에서 지원하는 구성 매개 변수가 있는 JSON 개체입니다. 이 경우, `params` 오브젝트에는 최소한 으로 전달된 이미지 제공 URL이 있어야 합니다. `serverUrl` 속성, 비디오 서버 URL이 로 전달됨 `videoserverurl` 속성 및 초기 에셋 `asset` 매개 변수. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 빌드를 지연합니다. 호환성을 최대화하려면 `init()` 닫기 직전 메서드 `BODY` 태그 또는 본문에 `onload()` 이벤트.

   동시에 컨테이너 요소는 아직 웹 페이지 레이아웃의 일부가 아니어야 합니다. 예를 들어 다음을 사용하여 숨길 수 있습니다. `display:none` 스타일이 할당되었습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져오는 순간까지 초기화 프로세스를 지연합니다. 이 작업이 발생하면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에 전달한 다음 `init()` 메서드를 사용합니다. 이 예에서는 다음과 같이 가정합니다. `videoViewer` 는 뷰어 인스턴스이며, `s7viewer` 은 자리 표시자의 이름입니다. `DIV`, [!DNL http://s7d1.scene7.com/is/image/] 는 이미지 제공 URL이고, [!DNL http://s7d1.scene7.com/is/content/] 는 비디오 서버 URL이고, [!DNL Scene7SharedAssets/Glacier_Climber_MP4] 는 에셋입니다.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   다음 코드는 비디오 뷰어를 고정 크기로 임베드하는 간단한 웹 페이지의 전체 예입니다.

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**무제한 높이의 응답형 디자인 임베딩**

반응형 디자인 임베딩을 사용하면 일반적으로 웹 페이지에는 뷰어 컨테이너의 런타임 크기를 지정하는 일종의 유연한 레이아웃이 있습니다 `DIV`. 이 예의 경우, 웹 페이지에서 뷰어의 컨테이너를 허용한다고 가정해 봅시다 `DIV` 웹 브라우저 창의 크기를 40% 줄이려면 높이를 제한 없이 유지하십시오. 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 포함과 유사합니다. 유일한 차이점은 뷰어 크기를 명시적으로 정의할 필요가 없다는 것입니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. 컨테이너 DIV 정의.
1. 뷰어를 만들고 초기화하는 중입니다.

위의 모든 단계는 고정 크기 포함과 동일합니다. 컨테이너 추가 `DIV` 기존 &quot; 보유자&quot;에게 `DIV`. 다음 코드는 완전한 예입니다. 브라우저의 크기를 조정할 때 뷰어 크기가 어떻게 변경되는지, 뷰어 종횡비가 에셋과 어떻게 일치하는지 확인할 수 있습니다.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

다음 예제 페이지는 무제한 높이로 구현된 응답형 디자인의 실제 사용을 보여 줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[대체 데모 위치](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**폭 및 높이가 정의된 응답형 디자인 포함**

폭과 높이가 정의된 응답형 디자인 임베드가 있는 경우 웹 페이지 스타일이 달라집니다. 두 가지 크기가 모두 &quot; 홀더&quot;에 제공됩니다 `DIV` 브라우저 창에서 가운데로 맞춥니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소를 100%로 변환:

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

나머지 임베딩 단계는 제한되지 않은 높이를 갖는 응답형 디자인 임베딩과 동일합니다. 결과 예제는 다음과 같습니다.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Setter 기반 API를 사용하여 포함**

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 no-args 생성자를 사용할 수 있습니다. 해당 API를 사용하면 생성자는 매개 변수를 사용하지 않으며 를 사용하여 구성 매개 변수를 지정합니다. `setContainerId()`, `setParam()`, 및 `setAsset()` 별도의 JavaScript 호출을 사용한 API 메서드.

다음 예제는 setter 기반 API를 사용한 고정 크기 임베딩을 보여 줍니다.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
