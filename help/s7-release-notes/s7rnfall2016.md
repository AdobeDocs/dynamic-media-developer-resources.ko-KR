---
description: Adobe Marketing Cloud의 Adobe Experience Manager 솔루션에 포함된 Adobe Scene7 2016년 가을 릴리스에 대한 최신 릴리스 노트입니다.
seo-description: Adobe Marketing Cloud의 Adobe Experience Manager 솔루션에 포함된 Adobe Scene7 2016년 가을 릴리스에 대한 최신 릴리스 노트입니다.
seo-title: Scene7 2016 가을 릴리스
solution: Experience Manager
title: Scene7 2016 가을 릴리스
topic: Dynamic media
uuid: 3fddda65-0c6e-48ec-bd60-7e0ca59421a8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2263'
ht-degree: 0%

---


# Scene7 2016년 가을 릴리스{#scene-fall-release}

Adobe Marketing Cloud의 Adobe Experience Manager 솔루션에 포함된 Adobe Scene7 2016년 가을 릴리스에 대한 최신 릴리스 노트입니다.

## Scene7 2016 가을 릴리스 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

[!DNL Adobe Marketing Cloud]에 있는 [!DNL Adobe Experience Manager] 솔루션의 [!DNL Adobe Scene7] 2016년 가을 릴리스의 최신 릴리스 노트입니다.

* [일반](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7 Publishing System](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [뷰어(이미지 제공 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [뷰어(이미지 제공 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [뷰어(이미지 제공 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Scene7 HTML5 뷰어 SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Scene7 이미지 제공 6.3.2 및 이미지 렌더링 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 일반 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe은 향상된 성능을 통해 HTTP/2 컨텐츠 전달을 사용할 수 있음을 발표하게 되어 매우 기쁩니다.

[콘텐츠 FAQ ](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html)의 HTTP2 제공을 참조하십시오.

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

전체 설명서는 [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)을(를) 참조하십시오.

**새로운 기능, 개선 사항 및 버그 수정**

* [!DNL Adobe Scene7 Publishing System] 사용자 인터페이스에서 비디오 다시 자르기 기능을 제거했습니다.
* 필요한 경우 가능한 모든 Scene7 서버에 인증을 추가했습니다.
* 휴지통의 목록 보기와 관련된 버그 수정.
* 보안 문제로 인해 사용자 관리에서 **SPSAdmin** 사용자 기능 만들기를 제거했습니다.
* 이제 FTP WebAdmin이 OKTA 인증을 지원합니다.
* 새 Media Portal 사용자에 대해 만든 기본 암호 기능을 제거했습니다.
* 새 사용자를 추가할 때 생성된 임시 암호가 포함된 버그 수정 암호가 필요한 암호 요구 사항을 충족하지 않았습니다.
* WebAdmin 루트 디스크가 꽉 찼다는 문제가 해결되었습니다.
* 사용자 인터페이스에 즉시 반영되지 않는 사용자 비활성화 관련 버그가 수정되었습니다.
* 나중에 사용자를 다시 만들 수 없는 사용자 삭제와 관련된 버그 수정.
* 특정 설정을 제어하기 위해 인증이 포함되지 않은 새 Scene7 사용자에게 전송되는 시작 이메일과 관련된 버그 수정
* 이름에 특수 문자가 있는 폴더가 있는 경우 FTP 폴더 목록을 검색하지 못하는 버그를 수정했습니다.
* Scene7 환경을 위한 OKTA 서비스 공급자를 구성합니다.
* 뷰어 분석에 대한 Marketing Cloud 조직 ID 지원을 추가했습니다.
* Scene7 SAML 소비자가 구현되었습니다.

## 뷰어(이미지 제공 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

전체 설명서는 [뷰어 참조 안내서](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)를 참조하십시오.

**이미지 제공 5.5.3 버그 수정**

* RequireJS 및 DOJO 라이브러리와의 호환성

   뷰어 배포 중 통합된 SDK JS 캐싱.

## 뷰어(이미지 제공 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

전체 설명서는 [뷰어 참조 안내서](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)를 참조하십시오.

**이미지 제공 5.5.2 버그 수정**

* Windows 7의 Internet Explorer 11에서 비디오를 재생하지 못했습니다.
* `initialframe` HTML5 전자 카탈로그에 대한 모바일 장치의 세로 모드에 영향을 주지 않았습니다.

## 뷰어(이미지 제공 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

전체 설명서는 [뷰어 참조 안내서](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)를 참조하십시오.

**Image Serving 5.5.1의 새로운 기능, 개선 사항 및 버그 수정**

* 검색 기능이 포함된 HTML5 전자 카탈로그 뷰어.
* 대부분의 데스크탑 시스템에 기본 비디오 전달 방법으로 HLS 스트리밍 비디오 재생을 추가했습니다. Flash 기반의 HDS 비디오 스트리밍은 대체 재생 옵션으로 계속 사용할 수 있습니다.
* Chrome 브라우저를 실행하는 마우스 및 터치 입력이 모두 포함된 장치에 대한 지원을 추가했습니다.
* Analytics 통합에 Marketing Cloud 조직 ID 지원을 추가했습니다.
* AppMeasurement JavaScript 라이브러리를 버전 1.6.1으로 업데이트합니다.
* eCatalog 뷰어에서 오른쪽에서 왼쪽으로 방향 지원을 추가했습니다.
* `tip=0,-1,0`에서 범위를 벗어나는 오류가 발생하는 문제가 해결되었습니다.

**호환성 정보**

* Blackberry

   * 이전 AVS 세트와 호환되지 않습니다. 클라이언트가 재생을 허용하려면 AVS 세트를 다시 업로드해야 할 수도 있습니다.

* 일반

   * 사용자가 페이지를 확대/축소하면 브라우저 쪽 크기 조정으로 인해 UI 및 이미지가 흐려질 수 있습니다. 확대/축소에 따라 UI 서식이 잘못 표시될 수도 있습니다. 이것은 전체 화면으로 넘어간다.
   * 모바일 장치의 크기 제한으로 인해 혼합 미디어 뷰어는 포함된 견본 구성 요소를 탭하는 대신 슬라이드 제스처를 사용하여 포함된 이미지 세트의 프레임을 바꿉니다. 구성 요소는 시각적 표시기로 있습니다.
   * Internet Explorer 브라우저와 일부 터치 장치에서는 전체 화면 모드가 장치 화면을 차지하지 않습니다. 대신 응용 프로그램의 크기를 브라우저 창의 크기로 조정합니다.
   * 닫기 단추는 iOS 8.0 및 8.1에서 작동하지 않지만 iOS 8.2에서는 더 이상 발생하지 않습니다.

* Galaxy SIII

   * 확대/축소 및 eCatalog HTML5 뷰어에서 메모리 누수가 발생했습니다. 프레임 간을 계속 탐색하면 브라우저가 충돌할 수 있습니다.
   * 뷰어를 두 번 누르면 브라우저 쪽 크기 조정을 사용하는 뷰어만 확대하지 않고 전체 페이지가 확대/축소할 수 있습니다.

* Galaxy S4

   * 브라우저 설정에서 전체 화면을 선택한 상태에서 장치를 세로 모드에서 태블릿으로 감지했습니다.

* Galaxy Nexus

   * 뷰어를 두 번 누르면 브라우저 쪽 크기 조정을 사용하는 뷰어만 확대하지 않고 전체 페이지가 확대/축소할 수 있습니다.

* Galaxy Nexus 10 및 Galaxy Tablet

   * 세로 및 가로 방향의 잘못된 페이지 스프레드를 보여주는 eCatalog.

* HTC 모바일 장치

   * HTC 모바일 장치를 통해 기본 손가락을 모으고 펴서 확대/축소를 비활성화하지 못하는 것이 HTC UI 래퍼(HTC Sense)의 &quot;기능&quot;이라는 사실이 발견되었습니다. 뷰어에서 &quot;확대/축소&quot; 제스처를 사용할 때 전체 페이지가 확대/축소될 수 있습니다. 두 번 누르기를 대신 사용하는 것이 좋습니다.
   * 이미지 맵이 작고 서로 가까운 경우 이미지 맵 아이콘이 겹칠 수 있습니다.

* HTML5 비디오

   * Internet Explorer 9:사용자 정의 포스터 이미지는 표시되지 않습니다.
   * `IntialBitRate` 수정자는 소프트웨어 HLS 및 Flash HDS 재생에서만 지원됩니다. 재생이 기본 플레이어를 사용하는 경우에는 작동하지 않습니다.
   * 현재 OGG 및 WebM 점진적 재생은 지원되지 않습니다.
   * 브라우저 크기 조정으로 인해 비디오 플레이어가 잘못된 크기로 표시될 수 있습니다(Windows OS 제어판 표시 설정 포함).
   * Safari에서 HLS 스트리밍을 사용하는 비디오 검색이 일관되지 않을 수 있습니다.

* Internet Explorer

   * 지금은 quirks 모드가 지원되지 않습니다.
   * 현재 호환성 모드는 지원되지 않습니다.
   * 지금은 모바일의 Internet Explorer가 지원되지 않습니다.

* iOS

   * 큰 eCatalog를 사용하면 iPad 2에서 브라우저 충돌이 발생할 수 있습니다.
   * iPhone 6+ 전화기는 뷰어에서 태블릿으로 감지됩니다.

* Safari

   * Safari 6.1 이상:인터넷 플러그인 설정으로 인해 Flash 비디오 재생이 불가능할 수 있습니다.
   * Safari에서 HLS 스트리밍을 사용하는 비디오 &quot;검색&quot;이 일치하지 않을 수 있습니다.
   * HLS 스트리밍을 사용하여 Safari 6에서 비디오를 종료할 수 없습니다.

**알려진 문제 및 제한 사항**

* `iscommands`의 이미지 제공 수정자는 설계별로 `req=set` 요청에 추가되지 않습니다. 이미지 표시에만 영향을 주는 수정자만 제대로 작동합니다. 크기에 영향을 주는 수정자는 복잡한 자산에 사용해야 합니다. 예:

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [FlyoutIE9] 는 마우스를 놓은 후에도 간혹 화면에 남아 있습니다.
* 브라우저 크기를 조정하면 크기를 잘못 조정할 수 있습니다.
* iPad 2:대형 eCatalog 에셋은 iOS에서 Safari에 충돌이 발생합니다.
* 모든 뷰어

   * 워터마크, 난독화 및 잠금은 지원되지 않습니다.
   * 이미지 사전 설정은 지원되지 않습니다.
   * 현재 `display:none` CSS를 사용하거나 부모 노드에서 동적으로 분리하여 DOM에서 뷰어를 추가하거나 제거할 수 없습니다.

* HTML5 모든 뷰어

   * 표에 뷰어를 포함하면 뷰어의 크기가 잘못되거나 기본 전체 화면 모드가 아닌 상태에서 뷰어가 배치됩니다. 대신 DIV를 사용하는 것이 좋습니다.
   * 코드에 명시적 인스턴스 이름이 있는 매개 변수에는 URL의 인스턴스 이름과 덮어쓰여져야 합니다(예: `zoomView.iconfeffect=0`).
   * 현재 이미지 제공 명령 자르기는 지원되지 않습니다.
   * [닫기] 단추는 뷰어가 하위 창에 열려 있는 경우에만 작동합니다.
   * `iscommands` 수정자는 이미지 크기에 영향을 주는 이미지 제공 수정자를 지원하지 않습니다.

* HTML5 전자 카탈로그

   * 다른 HTML 페이지로 이동하여 돌아오면 뷰어가 첫 번째 페이지로 다시 재설정되는 경우가 있습니다.
   * iOS 장치를 회전하면 페이지 레이아웃이 잘못 표시되는 경우가 있습니다. 페이지를 확대하여 레이아웃을 수정합니다.
   * 다중 페이지 스프레드에서 가장 왼쪽 페이지에만 내부 링크가 있습니다. 세로 모드의 모바일 장치에 영향을 줍니다.
   * DigitalFrame 링크는 다중 페이지 스프레드에서 가장 왼쪽 페이지에만 연결됩니다. 세로 모드의 모바일 장치에 영향을 줍니다.
   * 브라우저 제한 사항으로 인해 IE9에서는 인쇄 기능을 사용할 수 없습니다.

* HTML5 혼합 미디어

   * 사운드트랙 재생은 현재 지원되지 않습니다.

* HTML5 Social

   * 보내는 이메일에서 축소판을 제대로 렌더링하려면 `serverurl` 수정자에 절대 URL이 있어야 합니다.

* HTML5 비디오

   * 포스터 이미지에 &quot;최대 크기&quot; 오류가 발생할 수 있습니다. 회사는 이미지 제공 게시에 대한 제한 설정을 늘려야 할 수 있습니다.
   * HTML 페이지를 호스팅하는 것이 외부 서버(Scene7 서버가 아님)에서 제공되는 경우 비디오 캡션을 사용하려면 회사 규칙 집합이 필요합니다. 도움이 필요하면 Adobe 지원 센터에 문의하십시오.
   * Analytics 추적은 버퍼링으로 인해 잘못된 재생 비율을 보고할 수 있습니다.
   * iPad 또는 Android 장치에서는 포스터 이미지 대신 검정 프레임이 표시될 수 있습니다.
   * iPad 또는 Android 장치에서 뷰어를 로드하는 동안 검정 프레임이 깜박일 수 있습니다.
   * 배경이 iPad 장치에서 흰색/투명으로 설정되어 있으면 VideoPlayer 구성 요소의 측면에 검정 테두리가 표시됩니다.
   * iOS 7을 사용하여 iPad에서 비디오의 마지막 프레임이 왜곡될 수 있습니다.
   * Chrome, Firefox 및 Internet Explorer 브라우저의 HLS 스트리밍 모드에서 비디오를 검색하는 동안 Macromedia가 가끔 차단될 수 있습니다.
   * 처음으로 Microsoft Edge 브라우저에 포스터 이미지가 표시되지 않을 수 있습니다.
   * 점진적 재생이 사용될 때 Internet Explorer 9에서 비디오가 로드된 후 포스터 이미지가 숨겨질 수 있습니다.

## Scene7 HTML5 뷰어 SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

사용자 안내서는 클라이언트 설치의 Adobe HTML5 뷰어 SDK 폴더에 있습니다. 구성 요소 API 설명서는 클라이언트 설치의 docs 하위 폴더에 있습니다.

**3.0.2 버그 수정**

* VideoPlayer - Windows 7의 Internet Explorer 11에서 비디오를 재생하지 못했습니다.
* TableOfContents - `initialframe`은(는) HTML5 전자 카탈로그 뷰어에 대한 모바일 장치의 세로 모드에 영향을 주지 않았습니다.

**3.0.1의 새로운 기능, 개선 사항 및 버그 수정**

* 일반

   * 대부분의 데스크탑 시스템에 기본 비디오 전달 방법으로 HLS 스트리밍 비디오 재생을 추가했습니다. Flash 기반의 HDS 비디오 스트리밍은 대체 재생 옵션으로 계속 사용할 수 있습니다.
   * eCatalog 뷰어에서 새 검색 기능을 지원하기 위해 SearchManager, SearchPanel, SearchEffect 및 SearchButton 구성 요소가 추가되었습니다.
   * Chrome 브라우저에서 마우스 및 터치 입력이 모두 실행되는 장치에 대한 지원을 추가했습니다.
   * OS의 향후 버전을 지원하기 위해 Android 버전 감지를 리팩토링했습니다.
   * eCatalog 특정 SDK 구성 요소에서 오른쪽에서 왼쪽으로 표기하는 방향으로 지원을 추가할 수 있습니다.

* ControlBar

   * 사용 가능한 폭에 맞지 않는 ControlBar 내용에 대한 선택적 스크롤을 추가했습니다.

* FlyoutzoomView

   * `tip=0,-1,0`에서 범위를 벗어나는 오류가 발생하는 문제가 해결되었습니다.

**호환성 정보**

* Android 4.x

   * 기본값을 사용하지 않도록 설정하려면 구성 요소에 대해 다음 CSS 규칙을 추가해야 합니다.

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * AVS 세트에서 비트율 스트림을 변경할 때 비디오 재생이 중단될 수 있습니다.

* Chrome

   * 구성 요소를 다시 빌드하도록 하는 모든 API 호출은 Chrome의 내부 캐싱으로 인해 무시될 수 있습니다.

* Galaxy SIII

   * 뷰어가 전체 화면으로 로드되지 않는 경우가 있습니다.
   * 현재 Pageview에서는 장치에서 메모리 누수가 발생합니다.
   * 브라우저 측면 크기 조절이 활성화되면 두 번 누르면 뷰어와 페이지가 확대됩니다.

* Galaxy Nexus

   * 일부 보기 구성 요소 위에 표시되는 객체입니다.
   * 브라우저 측면 크기 조절이 활성화되면 두 번 누르면 뷰어와 페이지가 확대됩니다.

* iPad 3

   * iPad 3의 기본 해상도는 2048x1536입니다. 이렇게 하면 회사의 IS 게시, 이미지 크기 제한이 그보다 낮게 설정된 경우 표시 문제가 발생할 수 있습니다.

* iPhone4

   * 페이지를 스크롤한 후 아이콘 효과 재생 아이콘이 재생 아이콘으로 바뀝니다.

* Internet Explorer

   * IE 10 이전 전체 화면 모드는 전체 화면을 차지하지 않으며 브라우저 창의 크기로 애플리케이션 크기를 조정합니다.
   * Quirks 렌더링 모드는 지원되지 않습니다.
   * 지금은 모바일의 Internet Explorer가 지원되지 않습니다.
   * 비동기적으로 포함된 경우 Util.js를 로드하지 못할 수 있습니다.
   * IconEffect 아이콘은 SpinView 및 ZoomView 구성 요소에서 클릭 이벤트를 차단합니다.

* 기본 디바이스 비디오 플레이어

   * VideoPlayer가 장치의 기본 플레이어를 호출하는 데 사용되는 경우 VideoPlayer를 통해 UI 구성 요소를 레이어하는 기능이 지원되지 않습니다.
   * Safari 6에서는 기본 모드에서 비디오 재생이 일관되지 않습니다.
   * 기본 재생은 페이지를 스크롤한 후 재생 아이콘을 재생 아이콘으로 바꿉니다.

* 터치 장치

   * 전체 화면 모드는 전체 장치 화면을 차지하지 않으며 브라우저 창의 크기로 응용 프로그램의 크기를 조정합니다.
   * 사용자 정의 커서는 터치 장치에서 작동하지 않습니다.
   * 현재는 터치 장치에서 페이지 크기 조절이 지원되지 않습니다. HTML5 뷰어를 포함하려면 적절한 설정을 갖는 뷰포트 메타 태그가 필요합니다.

* Xoom

   * 브라우저 측면 크기 조절이 활성화되면 두 번 누르면 뷰어와 페이지가 확대됩니다.

**알려진 문제 및 제한 사항**

* 모든 구성 요소

   * 버전 2.7.2 및 이전 버전에서는 `insertBefore()` API를 사용하여 일부 구성 요소가 DOM에 추가되었습니다. 그 결과 구성 요소 인스턴스가 다른 구성 요소를 기준으로 만들어지는 시기에 관계없이 이러한 구성 요소는 스택 순서의 맨 아래에 배치됩니다. 2.8.1 릴리스에서는 모든 구성 요소가 현재 `appendChild()` API를 사용하고 있습니다. 즉, 구성 요소 스택 순서가 인스턴스 생성 순서와 일치하게 됩니다.

   * `iscommand` 수정자를 사용하여 이미지 알파 채널 형식을 설정할 수 없습니다. 구성 요소 `FMT` 매개 변수를 대신 사용하십시오.
   * 지금은 CSS 변형 속성이 지원되지 않습니다.

* 터치 장치

   * 터치 장치에서 손가락을 모으고 펴서 동작해도 확대/축소 이벤트가 생성되지 않습니다.

* 컨테이너

   * 컨테이너의 테두리, 패딩 및 여백은 지원되지 않습니다. Adobe에서는 부모 DIV에 스타일 요소를 추가하는 것이 좋습니다.
   * 컨테이너 크기를 명시적으로 설정해야 합니다. 그렇지 않으면 구성 요소의 크기가 올바르게 조정될 수 있습니다.

* 구성 요소 인쇄

   * 브라우저 제한 사항으로 인해 Internet Explorer 9에서는 인쇄 구성 요소가 용지에서 내용의 크기를 적절하게 조정하지 못할 수 있습니다.

* IconEffect 구성 요소

   * `autohide`이(가) 비활성화되어 있는 경우 IconEffect는 Internet Explorer에서 스크립트 오류를 생성합니다(`0`로 설정).

* ImageMapEffect 구성 요소

   * 보기 구성 요소에서 이미지를 이동할 때 위치 변경 아이콘으로 지연을 참조하십시오.

* MediaSet 구성 요소

   * 인라인 에셋은 URL과 동일한 인코딩을 요청합니다.

* NavigationView 구성 요소

   * 현재 구성 요소는 크기 조정을 지원하지 않습니다.

* PageScrubber 구성 요소

   * iPhone 5에서 PageScrubber 버블이 텍스트로 설정된 경우 트랙을 따라 단추를 이동할 때 결함이 표시됩니다. 스타일에서 `-webkit-background-clip: content;`을(를) 사용하면 문제가 해결됩니다.

* SpinView 구성 요소

   * 이미지가 회전하는 동안 스와이프 제스처를 수행하고 장치를 회전하면 SpinView가 정지되는 경우가 있습니다.

* 견본 구성 요소

   * 경계 밖 견본을 선택하면 2개의 밝은 영역이 표시됩니다.
   * `selectSwatch()` 메서드를 사용한 자동 스크롤이 제대로 작동하지 않습니다.

* VideoPlayer

   * [폴백]이 [자동]으로 설정된 상태로 [검색]이 100%로 설정된 경우 비디오 프레임이 업데이트되지 않습니다.
   * Chrome, Firefox 및 Internet Explorer 브라우저의 HLS 스트리밍 모드에서 비디오를 검색하는 동안 경우에 따라 매크로가 차단될 수 있습니다.
   * 처음으로 Microsoft Edge 브라우저에 포스터 이미지가 표시되지 않을 수 있습니다.
   * 점진적 재생이 사용될 때 Internet Explorer 9에서 비디오가 로드된 후 포스터 이미지가 숨겨질 수 있습니다.

## Scene7 이미지 제공 6.3.2 및 이미지 렌더링 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC 유틸리티 - `downsample2x2` 플래그가 더 이상 지원되지 않습니다. 이 플래그는 IPS에서 더 이상 사용되지 않는 품질이 낮은 2x2 다운샘플러 입니다.
* CORS 헤더 - 현재, CORS 헤더는 `/is/content/` 요청에 대해 구성됩니다.

