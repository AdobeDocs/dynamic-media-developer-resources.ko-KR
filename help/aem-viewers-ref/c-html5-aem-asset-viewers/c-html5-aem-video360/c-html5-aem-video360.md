---
description: HTML5 Video360 뷰어는 H.264 형식으로 인코딩된 스트리밍 및 점진적 360 비디오를 재생하는 360도 비디오 플레이어로, Dynamic Media Classic 또는 AEM Dynamic Media에서 제공합니다.
solution: Experience Manager
title: 비디오360
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR 비디오
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2590'
ht-degree: 0%

---

# 비디오360{#video}

HTML5 Video360 뷰어는 Dynamic Media Classic 또는 AEM Dynamic Media에서 H.264 형식으로 인코딩된 스트리밍 및 점진적 360 비디오를 재생하는 360도 비디오 플레이어입니다.

360도 비디오(몰입형 비디오 또는 구형 비디오)는 옴니방향 카메라나 카메라 모음을 사용하여 모든 방향의 보기를 동시에 녹화하는 비디오 녹화입니다. 단일 비디오 및 응용 비디오 세트가 모두 지원됩니다. 뷰어는 외부 위치에서 호스팅되는 점진적 비디오 및 HLS 스트림 작업을 추가로 지원합니다.

360 비디오에 대한 권장 종횡비는 2:1입니다. 공간 사운드는 지원되지 않습니다. 이 뷰어는 360개의 비디오에서만 작동하도록 디자인되었습니다. 360이 아닌 비디오를 재생하려고 하면 비디오가 왜곡됩니다.

뷰어는 HTML5 비디오를 지원하는 데스크탑 및 모바일 웹 브라우저에서 모두 작동하도록 디자인되었습니다. 뷰어는 선택적 소셜 공유 도구를 지원합니다.

Video360 뷰어는 기본 시스템이 지원할 때마다 기본 구성에서 HTML5 스트리밍 비디오 재생을 HLS 형식으로 사용합니다. HTML5 스트리밍을 지원하지 않는 시스템에서 뷰어는 HTML5 점진적 비디오 제공으로 다시 폴백됩니다.

뷰어 유형은 517입니다.

## 데모 URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 시스템 요구 사항 {#section-b7270cc4290043399681dc504f043609}

[시스템 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)을 참조하십시오.

## Video360 뷰어 사용 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 뷰어는 런타임 시 뷰어가 다운로드한 기본 JavaScript 파일 및 도우미 파일 세트(단일 JavaScript에는 이 특정 뷰어, 자산 및 CSS)에 사용되는 모든 HTML5 Viewer SDK 구성 요소에 포함됩니다.

HTML5 Video360 뷰어는 IS-Viewers와 함께 제공된 프로덕션 준비 HTML 페이지를 사용하여 팝업 모드에서 또는 포함된 모드에서 둘 다 사용할 수 있으며, 이 페이지는 문서화된 API를 사용하여 Target 웹 페이지에 통합됩니다.

구성 및 스키닝은 이 안내서에서 설명하는 다른 뷰어의 구성과 유사합니다. 모든 스키닝은 사용자 지정(CSS) 계단식 스타일 시트를 통해 수행됩니다.

모든 뷰어에 공통되는 [명령 참조 - 구성 속성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어에 공통되는 명령 참조 - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)를 참조하십시오.

360 비디오 컨텐츠를 사용하려면 표준 비360 비디오보다 높은 인코딩 설정이 필요합니다. 즉, 동일한 인지 품질을 얻으려면 360개의 콘텐츠가 360이 아닌 비디오보다 해상도가 높아야 합니다. 360 비디오에 대해 다음 응용 비디오 사전 설정 설정을 고려하는 것이 좋습니다.

* 720p, 2500kbps
* 1080p, 5000kbps
* 1440p, 6600kbps

그러나 고품질 설정으로 인코딩된 비디오를 제공하려면 최종 사용자의 장치에서 높은 대역폭 연결이 필요합니다.

## Video360 뷰어와 상호 작용 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer는 재생/일시 정지 단추, 비디오 스크러버 비디오 시간 버블, 재생 시간/총 시간 표시기, 볼륨 제어 및 전체 화면 단추와 같은 비디오 재생에 대한 표준 사용자 인터페이스 컨트롤 집합을 제공합니다. 이러한 모든 컨트롤은 뷰어 사용자 인터페이스 맨 아래에 있는 컨트롤 막대로 그룹화됩니다.

터치 장치에서는 장치의 하드웨어 단추를 사용해야만 볼륨을 제어할 수 있으므로 볼륨 컨트롤이 사용자 인터페이스에서 숨겨집니다.

뷰어가 팝업 모드에서 작동하면 사용자 인터페이스에서 전체 화면 단추를 사용할 수 없습니다.

뷰어는 다양한 소셜 미디어 공유 도구도 지원합니다. 사용자 인터페이스에서 사용자가 클릭하거나 탭할 때 공유 도구 모음으로 확장되는 단일 단추로 사용할 수 있습니다. 공유 도구 모음에는 Facebook, Twitter, 이메일 공유, 포함 코드 공유 및 링크 공유와 같이 지원되는 각 유형의 공유 채널에 대한 아이콘이 포함되어 있습니다. 전자 메일 공유, 포함 공유 또는 링크 공유 도구가 활성화되면 뷰어에 해당 데이터 입력 양식이 있는 모달 대화 상자가 표시됩니다. facebook 또는 Twitter이 호출되면 뷰어는 소셜 미디어 서비스에서 표준 공유 대화 상자로 사용자를 리디렉션합니다. 또한 공유 도구가 활성화되면 비디오 재생이 자동으로 일시 중지됩니다. 웹 브라우저 보안 제한 사항으로 인해 전체 화면 모드에서는 공유 도구를 사용할 수 없습니다.

이 뷰어는 VR 헤드셋(Oculus Go 및 Oculus Rift 등), VR HMD(Head-Mounted display) 마운트(Google Bosboard 등) 및 비VR 지원 장치(예: 데스크탑 브라우저, 태블릿 및 VR HMD 마운트에 연결되지 않은 휴대폰 등)에서 360 비디오 재생을 지원합니다.

VR 헤드셋에서 360 비디오 콘텐츠를 보는 데 추가 구성이 필요하지 않습니다. 뷰어는 VR 헤드셋의 존재를 자동으로 감지하고 비디오 콘텐츠 위에 &quot;VR&quot; 단추를 표시합니다. 이 &quot;VR&quot; 단추를 활성화하면 비디오 렌더링이 VR 모드로 전환됩니다. 뷰어는 WebVR을 지원하는 브라우저에서만 VR 렌더링을 지원합니다.

VR HMD를 사용하려면 뷰어의 구성에서 `Video360Player.vrrender` 한정자를 `1`(으)로 설정해야 하여 스테레오스코픽 렌더링을 강제 적용합니다.

VR 헤드셋 및 VR HMD 마운트 POV 변경은 헤드셋 이동에 응답하여 수행되며 다른 재생 컨트롤은 VR 모드로 제공되지 않습니다.

VR이 아닌 지원 장치에서 360 비디오를 보는 경우 최종 사용자는 마우스, 터치 또는 키보드를 사용하여 비디오 재생 및 보기 지점을 제어할 수 있습니다.

뷰어는 터치 스크린 및 마우스를 사용하는 Windows 장치에서 터치 입력과 마우스 입력을 모두 지원하지만 Chrome, Internet Explorer 11 및 Edge 웹 브라우저만 지원합니다.

뷰어는 키보드로 액세스할 수 있습니다. [키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)을 참조하십시오.

## Video360 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 동작에 대한 요구 사항이 다릅니다. 경우에 따라 웹 페이지에서 를 클릭하면 별도의 브라우저 창에서 뷰어가 열리는 링크를 제공합니다. 다른 경우에는 뷰어를 호스팅 페이지에 직접 포함해야 합니다. 후자의 경우, 웹 페이지에는 정적 페이지 레이아웃이 있을 수 있으며, 다른 장치 또는 다른 브라우저 창 크기에 대해 다르게 표시되는 응답형 디자인을 사용할 수 있습니다. 이러한 요구 사항을 수용하기 위해 뷰어는 다음 세 가지 기본 작업 모드를 지원합니다. 팝업, 고정 크기 포함 및 반응형 디자인 포함.

태블릿 및 모바일 장치에서 동일한 페이지에 여러 비디오를 포함할 수 있습니다. 대부분의 경우 한 번에 하나의 비디오만 재생할 수 있습니다. 사용자가 한 비디오를 재생하기 시작한 다음 다른 비디오를 재생하려고 하면 첫 번째 비디오가 자동으로 일시 정지됩니다. 자동 일시 중지된 비디오는 현재 재생 시간을 기억하므로 사용자가 항상 다시 돌아가서 재생을 재개할 수 있습니다. 이 규칙은 Android 4.x 장치의 Chrome 브라우저에서 비디오를 동시에 재생할 수 있는 유일한 예외입니다.

**팝업 모드 기본 정보**

팝업 모드에서 뷰어는 별도의 웹 브라우저 창이나 탭에서 열립니다. 브라우저 크기가 조정되거나 장치 방향이 변경되는 경우 전체 브라우저 창 영역을 사용하고 조정됩니다.

이 모드는 모바일 장치에 가장 일반적입니다. 웹 페이지는 `window.open()` JavaScript 호출을 사용하여 뷰어를 로드하거나, 올바르게 구성된 `A` HTML 요소 또는 기타 적절한 메서드를 사용합니다.

팝업 작업 모드에 기본 HTML 페이지를 사용하는 것이 좋습니다. 이 이름을 [!DNL Video360Viewer.html]이라고 하며, 표준 IS-Viewers 배포의 [!DNL html5/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

사용자 지정 CSS를 적용하여 시각적 사용자 지정을 수행할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**고정 크기 포함 모드 및 응답형 디자인 포함 모드 정보**

포함된 모드에서 뷰어가 기존 웹 페이지에 추가되며, 이 페이지에 이미 뷰어와 관련이 없는 일부 고객 콘텐츠가 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지의 부동산의 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치를 위한 웹 페이지 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 응답형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 고정 크기 포함이 사용됩니다. 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

응답형 디자인 임베딩에서는 뷰어가 컨테이너 `DIV`의 크기 변경에 응답하여 런타임 시 크기를 조정해야 할 수 있다고 가정합니다. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

응답형 디자인 포함 모드에서 뷰어는 웹 페이지의 컨테이너 `DIV`의 크기 조절 방식에 따라 다르게 동작합니다. 웹 페이지가 컨테이너 `DIV`의 너비만 설정하고 높이를 제한을 두지 않는 경우 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능을 사용하면 측면에 패딩되지 않고 자산이 보기에 완벽하게 맞습니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 웹 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적입니다.

그렇지 않으면 웹 페이지가 뷰어의 컨테이너 `DIV`에 대한 너비와 높이를 모두 설정하면 뷰어가 해당 영역을 채우고 웹 페이지 레이아웃이 제공하는 크기를 따릅니다. 좋은 예는 뷰어를 모달 오버레이에 포함하는데, 이 오버레이는 웹 브라우저 창 크기에 따라 크기가 조정됩니다.

**고정 크기 포함**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일 추가.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 [!DNL Video360Viewer.js]를 포함해야 합니다. [!DNL Video360Viewer.js] 파일은 표준 IS-Viewers 배포의 [!DNL html5/js/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Adobe Dynamic Media Classic 서버 중 하나에 뷰어가 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>페이지에서 기본 뷰어 JavaScript `include` 파일만 참조하면 됩니다. 런타임 시 뷰어의 논리로 다운로드할 수 있는 웹 페이지 코드에서 추가 JavaScript 파일을 참조해서는 안 됩니다. 특히 `/s7viewers` 컨텍스트 경로(소위 통합 SDK `include`)에서 뷰어가 로드한 HTML5 SDK `Utils.js` 라이브러리를 직접 참조하지 마십시오. 이유는 `Utils.js` 또는 유사한 런타임 뷰어 라이브러리의 위치가 뷰어의 논리에 의해 완전히 관리되고 뷰어 릴리스 간에 위치가 변경되기 때문입니다. Adobe은 이전 버전의 보조 뷰어 `includes`를 서버에 유지하지 않습니다.
>
>
>따라서 페이지에서 뷰어가 사용하는 보조 JavaScript `include`에 직접 참조를 지정하면 새 제품 버전이 배포될 때 나중에 뷰어 기능이 중단됩니다.

1. `DIV` 컨테이너를 정의합니다.

   뷰어를 표시할 페이지에 빈 `DIV` 요소를 추가합니다. 이 ID가 나중에 뷰어 API로 전달되므로 `DIV` 요소에는 해당 ID가 정의되어 있어야 합니다. DIV의 크기는 CSS를 통해 지정됩니다.

   자리 표시자 `DIV`는 위치하는 요소입니다. 즉, `position` CSS 속성이 `relative` 또는 `absolute`로 설정되어 있습니다.

   전체 화면 기능이 Internet Explorer에서 제대로 작동하려면 DOM에 자리 표시자 `DIV`보다 높은 스태킹 순서를 갖는 다른 요소가 없는지 확인하십시오.

   다음은 정의된 자리 표시자 `DIV` 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 뷰어 크기 설정

   `.s7video360viewer` 최상위 CSS 클래스에 대해 절대 단위로 선언하거나 `stagesize` 한정자를 사용하여 뷰어의 정적 크기를 설정할 수 있습니다.

   HTML 페이지에서 직접 또는 사용자 지정 뷰어 CSS 파일에서 크기를 조정할 수 있습니다. 이 파일은 나중에 AEM Assets의 뷰어 사전 설정 레코드에 지정되거나, 요청 시 또는 `style` 명령을 사용하여 명시적으로 전달할 수 있습니다.

   CSS를 사용하여 뷰어의 스타일을 지정하는 방법에 대한 자세한 내용은 [Video360 뷰어 사용자 지정](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)을 참조하십시오.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   AEM Assets - 온디맨드 의 뷰어 사전 설정 레코드에서 `stagesize` 수정자를 설정할 수 있습니다. 또는 다음과 같이 `params` 컬렉션을 사용하거나 명령 참조 섹션에 설명된 대로 API 호출로 뷰어 초기화 코드를 명시적으로 전달할 수 있습니다.

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   CSS 기반 접근 방식이 권장되며 이 예에서 사용됩니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.Video360Viewer` 클래스의 인스턴스를 만들고 모든 구성 정보를 해당 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 JSON 개체로 생성자에게 전달됩니다. 최소한 이 개체에는 뷰어 컨테이너 ID의 이름을 포함하는 `containerId` 필드가 있어야 하며, 뷰어에서 지원하는 구성 매개 변수와 함께 중첩된 `params` JSON 개체가 있어야 합니다.

   이 경우 `params` 개체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL 이상이 있어야 하며 초기 자산은 `asset` 매개 변수여야 합니다. JSON 기반 초기화 API를 사용하면 단일 코드 줄, `videoserverurl` 속성으로 전달된 비디오 서버 URL, `asset` 매개 변수로 초기 자산 및 `interactivedata` 속성으로 대화형 데이터로 뷰어를 만들고 시작할 수 있습니다. JSON 기반 초기화 API를 사용하면 단일 코드 행으로 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 DOM에 뷰어 컨테이너를 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 호환성을 최대화하려면 `BODY` 태그를 닫기 직전에 또는 body `onload()` 이벤트에서 `init()` 메서드를 호출하십시오.

   동시에 컨테이너 요소가 반드시 아직 웹 페이지 레이아웃의 일부일 필요는 없습니다. 예를 들어 지정된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 다시 레이아웃으로 가져오는 시점까지 초기화 프로세스를 지연합니다. 이렇게 되면 뷰어 로드가 자동으로 다시 시작됩니다.

   다음은 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 뷰어 인스턴스를 만드는 예입니다. 이 예제에서는 다음을 가정합니다.

   * 뷰어 인스턴스는 `video360Viewer`입니다.
   * 자리 표시자 `DIV`의 이름은 `s7viewer`입니다.
   * 이미지 제공 URL은 `https://s7d9.scene7.com/is/image`입니다.
   * 비디오 서버 URL은 `https://s7d9.scene7.com/is/content`입니다.
   * 자산이 `Viewers/space_station_360-AVS`입니다.

   ```
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   다음 코드는 고정된 크기의 Video360 Viewer를 포함하는 작은 웹 페이지의 전체 예입니다.

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**제한 없는 높이를 사용한 반응형 디자인 포함**

응답형 디자인 포함 기능을 사용할 경우, 일반적으로 웹 페이지에는 뷰어 컨테이너의 런타임 크기를 지시하는 유연한 레이아웃이 있습니다 `DIV`. 다음 예를 들어, 웹 페이지에서 뷰어의 컨테이너 `DIV`가 웹 브라우저 창 크기의 40%를 취할 수 있도록 허용하여 높이 제한이 없는 것으로 가정해 보겠습니다. 웹 페이지 HTML 코드는 다음과 같습니다.

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
1. 컨테이너 DIV를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 포함과 동일합니다. 기존 `"holder"` DIV에 컨테이너 DIV를 추가합니다. 다음 코드는 완전한 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되는지 및 뷰어 종횡비가 자산과 어떻게 일치하는지 확인합니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**너비와 높이가 정의된 응답형 포함**

너비와 높이가 정의된 응답형 포함의 경우 웹 페이지 스타일링이 다릅니다. 이 확장은 `"holder"` DIV에 두 크기를 모두 제공하고 브라우저 창에 배치합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
