---
description: 비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다. Scene7 Publishing System 또는 AEM Dynamic Media에서 제공됩니다.
keywords: responsive
seo-description: 비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다. Scene7 Publishing System 또는 AEM Dynamic Media에서 제공됩니다.
seo-title: 비디오
solution: Experience Manager
title: 비디오
topic: Dynamic media
uuid: 961a9b99-5892-4ee3-a2df-13e299f5d086
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2402'
ht-degree: 0%

---


# 비디오{#video}

비디오 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 비디오를 재생하는 비디오 플레이어입니다. Scene7 Publishing System 또는 AEM Dynamic Media에서 제공됩니다.

[시스템 요구 사항 및 사전 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)을 참조하십시오.

단일 비디오 세트와 응용 비디오 세트가 모두 지원됩니다. 또한 뷰어는 외부 위치에 호스팅된 점진적 비디오 및 HLS 스트림을 사용하여 작업을 지원합니다. HTML5 비디오를 지원하는 데스크탑 및 모바일 웹 브라우저 모두에서 작동하도록 설계되었습니다. 또한 이 뷰어는 비디오 컨텐츠, 비디오 장 탐색 및 소셜 미디어 공유 도구 위에 표시되는 선택적 자막을 지원합니다.

비디오 뷰어는 기본 시스템이 지원하는 경우 HTML5 스트리밍 비디오 재생을 기본 구성으로 사용합니다. HTML5 스트리밍을 지원하지 않는 시스템에서 뷰어는 HTML5 점진적 비디오 전달으로 돌아갑니다.

뷰어 유형 506입니다.

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## 비디오 뷰어 사용 {#section-f21ac23d3f6449ad9765588d69584772}

비디오 뷰어는 기본 JavaScript 파일 및 도우미 파일 세트를 나타냅니다. 단일 JavaScript는 이 특정 뷰어에서 사용하는 모든 뷰어 SDK 구성 요소, 자산 및 런타임에 뷰어가 다운로드한 CSS 구성 요소에 포함됩니다.

IS-뷰어와 함께 제공된 프로덕션 준비 HTML 페이지를 사용하여 팝업 모드에서 비디오 뷰어를 사용할 수 있습니다. 또는 포함된 모드에서 뷰어를 사용할 수 있습니다. 이 모드에서는 문서화된 API를 사용하여 대상 웹 페이지에 연결됩니다.

뷰어를 구성하고 스킨하는 작업은 다른 뷰어와 유사합니다. 모든 스키닝은 사용자 지정 CSS를 통해 수행됩니다.

모든 뷰어에 공통되는 [명령 참조 - 모든 뷰어에 공통되는 구성 특성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 비디오 뷰어와 상호 작용 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

비디오 뷰어는 재생/일시 정지 단추, 비디오 스크러버 비디오 시간 버블, 재생 시간/총 시간 표시기, 볼륨 컨트롤, 전체 화면 단추 및 닫힌 캡션 토글과 같은 비디오 재생을 위한 표준 사용자 인터페이스 컨트롤 세트를 제공합니다. 이러한 모든 컨트롤은 뷰어 사용자 인터페이스 아래쪽에 있는 컨트롤 막대로 그룹화됩니다.

터치 장치에서는 하드웨어 단추를 사용하여 볼륨을 제어할 수 있으므로 사용자 인터페이스에서 볼륨 컨트롤이 숨겨집니다.

뷰어가 팝업 모드에서 작동하면 사용자 인터페이스에서 전체 화면 단추를 사용할 수 없습니다.

비디오 장(chapter) 작업이 활성화되면 비디오 컨텐츠를 신속하게 탐색할 수 있습니다. 비디오 장은 비디오 스크러버 트랙에 마커로 표시되며 터치 시스템을 한 번 누르거나 마우스 롤에 장 제목 및 관련 설명을 표시합니다. 장 마커를 클릭하거나 장 설명 버블을 탭하여 특정 장을 검색할 수 있습니다.

뷰어는 터치 스크린과 마우스로 Windows 장치에서 터치 입력 및 마우스 입력을 모두 지원합니다. 그러나 이러한 지원은 Chrome, Internet Explorer 11 및 Edge 웹 브라우저에만 제한됩니다.

이 뷰어는 키보드로 완벽하게 액세스할 수 있습니다.

[키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)을 참조하십시오.

## 비디오 뷰어가 포함된 소셜 미디어 공유 도구 {#section-907d316fe1da4b87abb9775f02464704}

비디오 뷰어는 소셜 미디어 공유 도구를 지원합니다. 이 도구는 사용자 인터페이스에서 사용자가 클릭하거나 탭할 때 공유 도구 모음으로 확장되는 단일 단추로 사용할 수 있습니다.

공유 도구 모음에는 Facebook, Twitter, 이메일 공유, 포함 코드 공유 및 링크 공유와 같이 지원되는 각 유형의 공유 채널에 대한 아이콘이 포함되어 있습니다. 이메일 공유, 포함 공유 또는 링크 공유 도구가 활성화되면 뷰어는 해당 데이터 입력 양식이 있는 양식 대화 상자를 표시합니다. Facebook 또는 Twitter가 호출되면 뷰어는 소셜 미디어 서비스에서 사용자를 표준 공유 대화 상자로 리디렉션합니다. 또한 공유 도구가 활성화된 비디오 재생이 자동으로 일시 정지될 때도.

웹 브라우저 보안 제한 사항으로 인해 공유 도구를 전체 화면 모드에서 사용할 수 없습니다.

## 비디오 뷰어 {#section-6bb5d3c502544ad18a58eafe12a13435} 포함

웹 페이지마다 뷰어 비헤이비어에 대한 요구 사항이 다릅니다. 웹 페이지가 클릭되면 별도의 브라우저 창에서 뷰어를 여는 링크를 제공하는 경우가 있습니다. 다른 경우에는 호스팅 페이지에 뷰어를 직접 포함해야 합니다. 후자의 경우 웹 페이지에 정적 페이지 레이아웃이 있거나, 다른 장치 또는 다른 브라우저 창 크기에 대해 다르게 표시되는 반응형 디자인을 사용할 수 있습니다. 이러한 요구 사항을 수용하기 위해 뷰어는 3가지 기본 작업 모드를 지원합니다.팝업, 고정 크기 임베드 및 반응형 디자인 임베드.

동일한 페이지에 여러 비디오를 포함시키는 것은 태블릿 및 모바일 장치에서 지원됩니다. 대부분의 경우 한 번에 하나의 비디오만 재생할 수 있습니다. 사용자가 비디오 하나를 재생하고 다른 비디오를 재생하려고 하면 첫 번째 비디오가 자동으로 일시 정지됩니다. 자동 일시 중지된 비디오는 현재 재생 시간을 기억하므로 사용자는 언제든지 비디오로 돌아가 재생을 다시 시작할 수 있습니다. 이 규칙은 비디오를 동시에 재생할 수 있는 Android 4.x 장치의 Chrome 브라우저에 있습니다.

**팝업 모드 정보**

팝업 모드에서 뷰어는 별도의 웹 브라우저 창이나 탭에서 열립니다. 전체 브라우저 창 영역을 사용하고 브라우저 크기가 조정되거나 장치 방향이 변경될 경우에 맞춰 조정합니다.

이 모드는 모바일 장치에서 가장 일반적으로 사용됩니다. 웹 페이지는 `window.open()` JavaScript 호출, 적절히 구성된 `A` HTML 요소 또는 기타 적절한 방법을 사용하여 뷰어를 로드합니다.

팝업 작업 모드에 기본 HTML 페이지를 사용하는 것이 좋습니다. 이 이름은 [!DNL VideoViewer.html]이며 표준 IS-뷰어 배포의 [!DNL html5/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/html5/VideoViewer.html]

사용자 지정 CSS를 적용하여 시각적 사용자 지정을 실현할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**고정 크기 포함 모드 및 응답형 포함 모드 정보**

포함된 모드에서 뷰어는 기존 웹 페이지에 추가되며, 이 페이지에 이미 뷰어와 관련이 없는 일부 고객 컨텐츠가 있을 수 있습니다. 뷰어는 보통 웹 페이지의 부동산 중 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치의 웹 페이지 지향 및 장치 유형에 따라 자동으로 레이아웃을 조정하는 반응형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 크기 임베딩이 사용됩니다. 이 선택 사항은 정적 페이지 레이아웃을 갖는 웹 페이지에 가장 적합합니다.

응답형 디자인 임베드는 뷰어가 컨테이너 `DIV`의 크기 변경에 응답하여 런타임 시 크기를 조정해야 할 수 있다고 가정합니다. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

반응형 디자인 임베드 모드에서 뷰어는 웹 페이지의 컨테이너 크기 `DIV`에 따라 다르게 동작합니다. 웹 페이지가 `DIV` 컨테이너의 너비만 설정하고 높이를 제한하지 않은 경우 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 방법을 사용하면 측면 패딩 없이 에셋이 보기에 완벽하게 맞춰집니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적으로 사용됩니다.

그렇지 않은 경우 웹 페이지가 뷰어의 컨테이너 `DIV`에 대한 폭과 높이를 모두 설정하는 경우 뷰어는 해당 영역만 채우고 웹 페이지 레이아웃에서 제공하는 크기를 따릅니다. 예를 들어 뷰어를 모달 오버레이에 포함시켜 오버레이의 크기가 웹 브라우저 창의 크기에 따라 조정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 [!DNL FlyoutViewer.js]을(를) 포함해야 합니다. [!DNL FlyoutViewer.js] 파일은 표준 IS-Viewers 배포의 [!DNL html5/js/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>페이지에서 기본 뷰어 JavaScript `include` 파일만 참조하면 됩니다. 런타임에서 뷰어의 논리로 다운로드할 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조해서는 안 됩니다. 특히, 뷰어가 `/s7viewers` 컨텍스트 경로(소위 통합 SDK `include`)에서 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오. 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리의 위치가 뷰어의 논리로 완전히 관리되고 뷰어 릴리스 간에 위치가 변경되기 때문입니다. Adobe은 이전 버전의 보조 뷰어 `includes` 버전을 서버에 유지하지 않습니다.
>
>
>따라서 페이지 뷰어에서 사용하는 보조 JavaScript `include`에 직접 참조하면 새 제품 버전이 배포될 때 향후 뷰어 기능이 중단됩니다.

1. 컨테이너 DIV를 정의합니다.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. 이 ID는 나중에 뷰어 API로 전달되므로 DIV 요소에는 ID가 정의되어 있어야 합니다. DIV의 크기는 CSS를 통해 지정됩니다.

   자리 표시자 DIV는 배치된 요소입니다. 즉, `position` CSS 속성이 `relative` 또는 `absolute`로 설정되어 있습니다.

   전체 화면 기능이 Internet Explorer에서 제대로 작동하는지 확인합니다. 자리 표시자 DIV보다 높은 겹침 순서가 있는 다른 요소가 DOM에 없는지 확인합니다.

   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 뷰어 크기 설정

   `.s7videoviewer` 최상위 CSS 클래스에 대해 절대 단위로 선언하거나 수정자 `stagesize`를 사용하여 뷰어의 정적 크기를 설정할 수 있습니다.

   CSS에서 크기 조정을 HTML 페이지 또는 나중에 Scene7 Publishing System의 뷰어 사전 설정 레코드에 할당되거나 스타일 명령을 사용하여 명시적으로 전달되는 사용자 정의 뷰어 CSS 파일에 배치할 수 있습니다.

   CSS를 사용하여 뷰어의 스타일 지정에 대한 자세한 내용은 [비디오 뷰어 사용자 지정](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)을 참조하십시오.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음과 같이 Scene7 Publishing System의 뷰어 사전 설정 레코드에 `stagesize` 수정자를 설정하거나, 뷰어 초기화 코드를 `params` 컬렉션으로 명시적으로 전달하거나 명령 참조 섹션에 설명된 대로 API 호출로 전달할 수 있습니다.

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   CSS 기반 접근 방식이 권장되며 이 예에서 사용됩니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.VideoViewer` 클래스의 인스턴스를 만들고 모든 구성 정보를 해당 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 생성자에게 JSON 개체로 전달됩니다. 적어도 이 개체에는 뷰어에서 지원하는 구성 매개 변수를 사용하여 뷰어 컨테이너 ID의 이름을 유지하고 중첩된 `params` JSON 개체가 있는 `containerId` 필드가 있어야 합니다. 이 경우 `params` 개체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL 이상, `videoserverurl` 속성으로 전달된 비디오 서버 URL 및 `asset` 매개 변수로 초기 에셋이 있어야 합니다. JSON 기반 초기화 API를 사용하여 단일 코드 행을 사용하여 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 최대 호환성을 위해 닫는 `BODY` 태그 바로 앞 또는 본문 `onload()` 이벤트에서 `init()` 메서드를 호출합니다.

   이와 동시에 컨테이너 요소가 웹 페이지 레이아웃에 반드시 포함되어야 하는 것은 아닙니다. 예를 들어, 지정된 `display:none` 스타일을 사용하여 숨겨질 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 지연합니다. 이 경우 뷰어 부하가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고, 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 예제입니다. 이 예에서는 `videoViewer`이 뷰어 인스턴스이고, `s7viewer`은 자리 표시자 `DIV`의 이름이고, [!DNL http://s7d1.scene7.com/is/image/]은 이미지 제공 URL이고, [!DNL http://s7d1.scene7.com/is/content/]은 비디오 서버 URL이고, [!DNL Scene7SharedAssets/Glacier_Climber_MP4]는 자산이라고 가정합니다.

   ```
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

   다음 코드는 비디오 뷰어에 고정된 크기를 포함하는 간단한 웹 페이지의 완전한 예입니다.

   ```
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

**제한 없는 높이를 갖는 반응형 디자인 임베드**

반응형 디자인 임베딩을 사용하면 일반적으로 웹 페이지에는 뷰어 컨테이너의 런타임 크기를 지정하는 유연한 레이아웃이 있습니다 `DIV`. 이 예제의 경우 웹 페이지에서 뷰어의 컨테이너 `DIV`에 웹 브라우저 창 크기의 40%를 사용할 수 있으며 높이는 제한이 없다고 가정합니다. 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 임베딩과 매우 유사합니다.유일한 차이점은 뷰어 크기를 명시적으로 정의할 필요가 없다는 것입니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. 컨테이너 DIV를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 임베딩과 동일합니다. 기존 &quot; 보유자&quot; `DIV`에 `DIV` 컨테이너를 추가합니다. 다음 코드는 완전한 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되고 뷰어 종횡비가 에셋과 어떻게 일치하는지 볼 수 있습니다.

```
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

다음 예제 페이지에서는 제한이 없는 반응형 디자인 임베딩의 실제 사용을 보여줍니다.

[라이브 데모](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**폭 및 높이가 정의된 반응형 디자인 임베드**

폭 및 높이가 정의된 반응형 디자인을 포함하는 경우, 웹 페이지 스타일이 다릅니다.&quot; holder&quot; `DIV`에 두 크기를 모두 제공하고 브라우저 창에서 중앙에 배치합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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

나머지 임베드 단계는 제한이 없는 반응형 디자인 임베딩과 동일합니다. 결과 예는 다음과 같습니다.

```
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

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 인수 없음 생성자를 사용할 수 있습니다. 해당 API를 사용하는 생성자는 별도의 JavaScript 호출을 사용하여 `setContainerId()`, `setParam()` 및 `setAsset()` API 메서드를 사용하여 지정한 매개 변수와 구성 매개 변수를 가져오지 않습니다.

다음 예제에서는 setter 기반 API를 사용한 고정 크기 임베드 방법을 보여 줍니다.

```
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

