---
title: Scene7 2016년 가을 릴리스
description: '"Adobe Experience Cloud에 있는 Adobe Experience Manager 솔루션의 일부인 Adobe Scene7 2016년 가을 릴리스의 최신 릴리스 노트입니다."'
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '2209'
ht-degree: 0%

---

# Scene7 2016년 가을 릴리스{#scene-fall-release}

Adobe Experience Cloud에 있는 Adobe Experience Manager 솔루션의 Adobe Scene7 2016년 가을 릴리스 부분에 대한 최신 릴리스 노트입니다.

## Scene7 2016년 가을 릴리스 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

에 대한 최신 릴리스 노트 [!DNL Adobe Scene7] 2016년 가을 릴리스 정보 [!DNL Adobe Experience Manager] 의 솔루션 [!DNL Adobe Experience Cloud].

* [일반](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [뷰어(이미지 제공 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [뷰어(이미지 제공 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [뷰어(이미지 제공 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 및 Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 일반 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe은 전반적인 성능이 개선된 HTTP/2 컨텐츠 제공을 발표하게 되었습니다.

자세한 내용은 [컨텐츠의 HTTP2 전달 FAQ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

전체 설명서에 대해서는 [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**새로운 기능, 개선 사항 및 버그 수정**

* 다음에서 비디오 리디렉션 기능이 제거됨 [!DNL Adobe Scene7 Publishing System] 사용자 인터페이스.
* 필요한 경우 가능한 모든 Scene7 서블릿에 인증이 추가되었습니다
* 휴지통의 목록 보기와 관련된 버그 수정.
* 제거됨 **Dynamic Media Classic(Scene7) 관리 만들기** 보안 문제로 인해 사용자 관리의 사용자 기능입니다.
* 이제 FTP WebAdmin이 OKTA 인증을 지원합니다.
* 새 Media Portal 사용자를 위해 만든 기본 암호 기능이 제거되었습니다.
* 새 사용자를 추가할 때 생성된 임시 암호와 관련된 버그 수정. 암호가 필요한 암호 요구 사항을 충족하지 않았습니다.
* WebAdmin 루트 디스크가 꽉 찼다는 문제가 해결되었습니다.
* 사용자 인터페이스에 즉시 반영되지 않는 사용자의 비활성화와 관련된 버그 수정.
* 사용자를 나중에 다시 만들 수 없도록 한 사용자 삭제와 관련된 버그 수정.
* 특정 설정을 제어하기 위해 인증을 포함하지 않은 새 Scene7 사용자에게 전송된 환영 이메일과 관련된 버그 수정.
* 이름에 특수 문자가 있는 경우 FTP 폴더 목록을 검색하지 못하는 버그가 수정되었습니다.
* Scene7 환경을 위한 OKTA 서비스 공급자를 구성합니다.
* Viewer Analytics에 대한 Experience Cloud 조직 ID 지원이 추가되었습니다.
* Scene7 SAML 소비자가 구현되었습니다.

## 뷰어(이미지 제공 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

전체 설명서에 대해서는 [뷰어 참조 안내서](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**이미지 제공 5.5.3에 대한 버그 수정**

* RequireJS 및 DOJO 라이브러리와의 호환성.

   뷰어 배포 중 통합 SDK JS 캐싱.

## 뷰어(이미지 제공 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

전체 설명서에 대해서는 [뷰어 참조 안내서](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**이미지 제공 5.5.2에 대한 버그 수정**

* Windows 7의 Internet Explorer 11에서 비디오를 재생하지 못했습니다.
* `initialframe` HTML5 eCatalog에 대한 모바일 장치의 세로 모드에 영향을 주지 않았습니다.

## 뷰어(이미지 제공 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

전체 설명서에 대해서는 [뷰어 참조 안내서](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Image Serving 5.5.1의 새로운 기능, 개선 사항 및 버그 수정**

* 검색 기능이 있는 HTML5 eCatalog viewer.
* 대부분의 데스크탑 시스템에 대한 기본 비디오 제공 방법으로 HLS 스트리밍 비디오 재생을 추가했습니다. Flash 기반 HDS 비디오 스트리밍은 여전히 대체 재생 옵션으로 사용할 수 있습니다.
* Chrome 브라우저를 실행하는 마우스 및 터치 입력이 모두 있는 장치에 대한 지원을 추가했습니다.
* Analytics 통합에 Experience Cloud 조직 ID 지원이 추가되었습니다.
* AppMeasurement JavaScript 라이브러리를 버전 1.6.1로 업데이트합니다.
* eCatalog 뷰어에서 오른쪽에서 왼쪽 방향으로의 지원을 추가했습니다.
* 이 문제가 `tip=0,-1,0` 가 범위를 벗어나는 오류가 발생했습니다.

**호환성 정보**

* BlackBerry®

   * 이전 AVS 세트와 호환하지 않습니다. 클라이언트가 재생을 허용하려면 AVS 세트를 다시 업로드해야 합니다.

* 일반

   * 브라우저 측 크기 조절을 사용하면 사용자가 페이지를 확대하면 UI 및 이미지가 흐릿해질 수 있습니다. 확대/축소에 따라 UI 형식이 잘못 표시될 수도 있습니다. 이 효과는 전체 화면으로 전달됩니다.
   * 모바일 장치의 크기 제한으로 인해 혼합 미디어 뷰어는 포함된 색상 견본 구성 요소를 탭하는 대신 슬라이드 제스처를 사용하여 포함된 이미지 세트의 프레임을 바꿉니다. 구성 요소는 시각적 표시기로 표시됩니다.
   * Internet Explorer 브라우저 및 일부 터치 장치에서 전체 화면 모드는 전체 장치 화면을 차지하지 않습니다. 대신 응용 프로그램의 크기를 브라우저 창 크기로 조정합니다.
   * 닫기 단추는 iOS 8.0 및 8.1에서 작동하지 않지만 iOS 8.2에서는 더 이상 발생하지 않습니다

* 갤럭시 SIII

   * 확대/축소 및 eCatalog HTML5 뷰어에서 메모리 누수가 표시됩니다. 프레임을 반복하여 탐색하면 브라우저가 충돌할 수 있습니다.
   * 뷰어를 두 번 탭하면 브라우저 측 크기 조절이 활성화된 뷰어가 아닌 전체 페이지가 확대/축소될 수 있습니다.

* Galaxy S4

   * 브라우저 설정에서 전체 화면이 선택된 세로 모드에서 태블릿으로 감지되었습니다.

* 갤럭시 넥서스

   * 뷰어를 두 번 탭하면 브라우저 측 크기 조절이 활성화된 뷰어가 아닌 전체 페이지가 확대/축소될 수 있습니다.

* 갤럭시 넥서스 10 및 갤럭시 태블릿

   * 세로 및 가로 방향이 있는 잘못된 페이지 분산을 표시하는 전자 카탈로그

* HTC 모바일 장치

   * HTC 모바일 장치 Adobe의 조사 결과에 따라 기본 확대/축소를 비활성화할 수 없는 것이 HTC UI 래퍼(HTC Sense)의 &quot;기능&quot;임을 보여줍니다. 이 문제로 인해 뷰어에서 &quot;확대/축소&quot; 제스처를 사용할 때 전체 페이지가 확대/축소될 수 있습니다. 대신 두 번 탭 사용을 추천합니다.
   * 이미지 맵이 작고 서로 가까운 경우 이미지 맵 아이콘이 겹칠 수 있습니다.

* HTML5 비디오

   * Internet Explorer 9: 사용자 지정 포스터 이미지가 표시되지 않습니다.
   * `IntialBitRate` 수정자는 소프트웨어 HLS 및 Flash HDS 재생에서만 지원됩니다. 재생이 기본 플레이어를 사용하는 경우에는 작동하지 않습니다.
   * OGG 및 WebM 점진적 재생은 현재 지원되지 않습니다.
   * 브라우저 크기 조절을 사용하면 비디오 플레이어가 잘못된 크기로 표시될 수 있습니다(Windows OS 컨트롤 패널 표시 설정 포함).
   * Safari에서 HLS 스트리밍을 사용하는 비디오 찾기가 일관되지 않을 수 있습니다.

* Internet Explorer

   * Quirks 모드는 현재 지원되지 않습니다.
   * 호환성 모드는 현재 지원되지 않습니다.
   * 모바일의 Internet Explorer는 현재 지원되지 않습니다.

* iOS

   * 큰 eCatalyst가 iPad 2에서 브라우저 충돌을 일으킬 수 있습니다.
   * iPhone 6+ 휴대폰은 뷰어에서 태블릿으로 감지됩니다.

* Safari

   * Safari 6.1 이상: 인터넷 플러그인 설정으로 인해 Flash 비디오가 재생되지 않을 수 있습니다.
   * Safari에서 HLS 스트리밍을 사용하는 비디오 &quot;찾기&quot;가 일치하지 않을 수 있습니다.
   * HLS 스트리밍을 사용하여 Safari 6에서 비디오를 종료할 수 없습니다.

**알려진 문제 및 제한 사항**

* 이미지 제공 수정자 `iscommands` 에 추가되지 않습니다. `req=set` 디자인별 요청. 이미지 표시에만 영향을 주는 수정자가 제대로 작동합니다. 크기에 영향을 주는 수정자는 복잡한 자산에 사용해야 합니다. For example,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [플라이아웃] IE9는 마우스를 끈 후 화면에 남아 있는 경우가 있습니다.
* 브라우저 크기 조절은 잘못된 크기 조절으로 이어집니다.
* iPad 2: 큰 eCatalog 자산이 iOS에서 Safari에 충돌합니다.
* 모든 뷰어

   * 워터마크, 난독화 및 잠금은 지원되지 않습니다.
   * 이미지 사전 설정은 지원되지 않습니다.
   * 를 사용하여 DOM에서 뷰어 추가 또는 제거 `display:none` CSS 또는 상위 노드에서 동적으로 분리되는 방식은 현재 지원되지 않습니다.

* HTML5 모든 뷰어

   * 표에 뷰어를 포함하면 비기본 전체 화면 모드에서 뷰어의 크기 조정이나 배치가 잘못될 수 있습니다. 대신 DIV를 사용하는 것이 좋습니다.
   * 코드에 명시적 인스턴스 이름이 있는 매개 변수에는 URL에 인스턴스 이름을 사용하고 덮어쓸 수 있습니다(예: `zoomView.iconfeffect=0`).
   * 현재 이미지 제공 명령 자르기가 지원되지 않습니다.
   * 닫기 단추는 뷰어가 하위 창에서 열려 있는 경우에만 작동합니다.
   * 다음 `iscommands` 수정자는 이미지 크기에 영향을 주는 이미지 제공 수정자를 지원하지 않습니다.

* HTML5 eCatalog

   * 다른 HTML 페이지로 이동하여 가끔 재설정하면 뷰어가 첫 번째 페이지로 다시 재설정됩니다.
   * iOS 장치를 회전하면 페이지 레이아웃이 잘못 표시되는 경우가 있습니다. 페이지를 확대하면 레이아웃이 수정됩니다.
   * 다중 페이지 스프레드에서 맨 왼쪽 페이지에만 연결된 내부 링크입니다. 세로 모드의 모바일 장치에 영향을 줍니다.
   * InitialFrame은 다중 페이지 스프레드에서 맨 왼쪽 페이지에만 연결됩니다. 세로 모드의 모바일 장치에 영향을 줍니다.
   * 브라우저 제한 사항으로 인해 IE9에서는 인쇄 기능을 사용할 수 없습니다.

* HTML5 MixedMedia

   * 사운드트랙 재생은 지원되지 않습니다.

* HTML5 소셜

   * 보내는 이메일에서 축소판을 올바르게 렌더링하려면 `serverurl` 수정자에게는 절대 URL이 있어야 합니다.

* HTML5 비디오

   * 포스터 이미지에 &quot;최대 크기&quot; 오류가 발생할 수 있습니다. 회사는 이미지 제공 게시에 대한 제한 설정을 늘려야 합니다.
   * 비디오 캡션을 사용하려면 외부 서버(Scene7 서버가 아님)에서 HTML 페이지를 호스팅하는 경우 회사 규칙 세트가 필요합니다. 도움이 필요하면 Adobe 지원 센터에 문의하십시오.
   * Analytics 추적은 버퍼링으로 인해 잘못된 재생 비율을 보고할 수 있습니다
   * 포스터 이미지 대신 검정 프레임이 iPad 또는 Android™ 장치에 표시될 수 있습니다.
   * iPad 또는 Android™ 장치에서 뷰어를 로드하는 동안 화면에서 검정 프레임이 깜박일 수 있습니다.
   * iPad 장치에서 배경이 흰색/투명하게 설정되면 VideoPlayer 구성 요소 측면에 검은색 테두리가 표시됩니다.
   * iOS 7을 사용하여 iPad에서 비디오의 마지막 프레임이 왜곡될 수 있습니다.
   * Chrome, Firefox 및 Internet Explorer 브라우저의 HLS 스트리밍 모드에서 비디오 검색 중에 비디오 찾기가 가끔 차단될 수 있습니다.
      * 처음 방문자가 Microsoft® Edge 브라우저에 포스터 이미지가 표시되지 않을 수 있습니다.
      * 점진적 재생이 사용될 때 Internet Explorer 9에서 비디오가 로드된 후 포스터 이미지가 숨겨질 수 있습니다.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

사용 안내서는 클라이언트 설치의 Adobe HTML5 Viewer SDK 폴더에 있습니다. 구성 요소 API 설명서는 클라이언트 설치의 docs 하위 폴더에 있습니다.

**3.0.2에 대한 버그 수정**

* VideoPlayer - Windows 7의 Internet Explorer 11에서 비디오를 재생하지 못했습니다.
* 목차 -  `initialframe` HTML5 eCatalog 뷰어에 대한 모바일 장치의 세로 모드에 영향을 주지 않았습니다.

**3.0.1의 새로운 기능, 개선 사항 및 버그 수정**

* 일반

   * 대부분의 데스크탑 시스템에 대한 기본 비디오 제공 방법으로 HLS 스트리밍 비디오 재생을 추가했습니다. Flash 기반 HDS 비디오 스트리밍은 여전히 대체 재생 옵션으로 사용할 수 있습니다.
   * eCatalog 뷰어의 새 검색 기능을 지원하도록 SearchManager, SearchPanel, SearchEffect 및 SearchButton 구성 요소가 추가되었습니다.
   * Chrome 브라우저에서 실행되는 마우스 및 터치 입력이 모두 있는 장치에 대한 지원을 추가했습니다.
   * 향후 OS 버전을 지원하도록 Android™ 버전 감지를 리팩터링했습니다.
   * eCatalog 특정 SDK 구성 요소에서 오른쪽에서 왼쪽 쓰기 방향에 대한 지원을 추가합니다.

* ControlBar

   * 사용 가능한 너비에 맞지 않는 ControlBar 내용에 대한 선택적 스크롤을 추가했습니다.

* FlyoutzoomView

   * 다음과 같은 경우 `tip=0,-1,0` 가 범위를 벗어나는 오류가 발생했습니다.

**호환성 정보**

* Android™ 4.x

   * 기본값을 비활성화하려면 파란색 강조 표시로 다음 CSS 규칙을 구성 요소에 추가해야 합니다.

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * AVS 세트에서 비트율 스트림을 변경할 때 비디오 재생이 중단될 수 있습니다.

* Chrome

   * 구성 요소를 다시 빌드하도록 하는 모든 API 호출은 Chrome의 내부 캐싱으로 인해 무시할 수 있습니다.

* 갤럭시 SIII

   * 뷰어가 전체 화면으로 로드되지 않는 경우가 있습니다.
   * 페이지 보기가 현재 장치의 메모리 누출로 인해 발생합니다.
   * 브라우저 측 크기 조절이 활성 상태일 때 두 번 탭하는 제스처가 뷰어와 페이지를 확대합니다.

* 갤럭시 넥서스

   * 일부 보기 구성 요소 위에 표시되는 객체.
   * 브라우저 측 크기 조절이 활성 상태일 때 두 번 탭하는 제스처가 뷰어와 페이지를 확대합니다.

* iPad 3

   * iPad 3의 기본 해상도는 2048x1536입니다. 이 해상도로 인해 회사의 IS 게시, 이미지 크기 제한이 더 낮게 설정된 경우 표시 문제가 발생할 수 있습니다.

* iPhone4

   * 페이지를 스크롤한 후 아이콘 효과 재생 아이콘이 재생 아이콘으로 대체되었습니다.

* Internet Explorer

   * IE 10 이상 버전의 전체 화면 모드는 전체 화면을 차지하지 않으며 대신 브라우저 창의 크기에 맞게 애플리케이션의 크기를 조정합니다.
   * Quirks 렌더링 모드가 지원되지 않습니다.
   * 모바일의 Internet Explorer는 현재 지원되지 않습니다.
   * 비동기식으로 포함된 경우 Util.js를 로드하지 못할 수 있습니다.
   * 아이콘 효과 아이콘 블록은 SpinView 및 ZoomView 구성 요소에서 클릭 이벤트를 호출합니다.

* 기본 장치 비디오 플레이어

   * VideoPlayer를 사용하여 장치의 기본 플레이어를 호출하면 VideoPlayer에서 UI 구성 요소를 계층화할 수 없습니다.
   * 기본 모드에서 비디오 재생이 Safari 6에서 일치하지 않습니다.
   * 기본 재생은 페이지를 스크롤한 후 재생 아이콘을 재생 아이콘으로 대체합니다.

* 터치 장치

   * 전체 화면 모드는 전체 장치 화면을 차지하지 않으며 대신 브라우저 창의 크기로 응용 프로그램의 크기를 조정합니다.
   * 사용자 지정 커서는 터치 장치에서 작동하지 않습니다.
   * 터치 장치에서 페이지 크기 조절은 현재 지원되지 않습니다. HTML5 뷰어를 포함하려면 적절한 설정을 사용하는 뷰포트 메타 태그가 필요합니다.

* Xoom

   * 브라우저 측 크기 조절이 활성 상태일 때 두 번 탭하는 제스처가 뷰어와 페이지를 확대합니다.

**알려진 문제 및 제한 사항**

* 모든 구성 요소

   * 버전 2.7.2 및 이전 버전에서 일부 구성 요소가 `insertBefore()` API. 따라서 이러한 구성 요소는 다른 구성 요소를 기준으로 구성 요소 인스턴스가 만들어진 시기에 상관없이 스태킹 순서의 맨 아래에 배치됩니다. 2.8.1 릴리스에서는 모든 구성 요소가 `appendChild()` API입니다. 즉, 구성 요소 스택 순서가 인스턴스 생성 순서와 일치합니다.

   * 사용 `iscommand` 이미지 알파 채널 형식을 설정하는 수정자가 지원되지 않습니다. 구성 요소 사용 `FMT` 매개 변수를 대신 사용하십시오.
   * CSS 변환 속성은 현재 지원되지 않습니다.

* 터치 장치

   * 터치 장치의 핀치 제스처가 확대/축소 이벤트를 생성하지 않습니다

* 컨테이너

   * 컨테이너의 테두리, 패딩 및 여백은 지원되지 않습니다. Adobe은 상위 DIV에 스타일 요소를 추가하는 것을 제안합니다.
   * 컨테이너 크기를 명시적으로 설정해야 합니다. 그렇지 않으면 구성 요소의 크기가 올바르게 될 수 있습니다.

* 구성 요소 인쇄

   * 브라우저 제한 사항으로 인해 Internet Explorer 9에서 인쇄 구성 요소는 용지에서 해당 컨텐츠의 크기를 적절하게 조정하지 못할 수 있습니다.

* IconEffect 구성 요소

   * IconEffect는 Internet Explorer에서 스크립트 오류를 생성합니다 `autohide` 비활성화되어 있습니다(으로 설정됨). `0`).

* ImageMapEffect 구성 요소

   * 보기 구성 요소에서 이미지를 패닝할 때 위치 조정 아이콘으로 지연하십시오.

* MediaSet 구성 요소

   * 인라인 자산은 URL과 동일한 인코딩을 요청합니다.

* NavigationView 구성 요소

   * 현재 구성 요소는 크기 조정을 지원하지 않습니다.

* PageScrubber 구성 요소

   * iPhone 5에서 PageScrubber 버블이 텍스트로 설정되면 트랙을 따라 단추를 이동할 때 아티팩트가 표시됩니다. 사용 `-webkit-background-clip: content;` 에서 스타일은 문제 주변에서 작동합니다.

* SpinView 구성 요소

   * 스핀 보기는 스와이프 제스처를 수행한 후 이미지가 회전하는 동안 장치를 회전하면 정지되는 경우가 있습니다.

* 색상 견본 구성 요소

   * 경계 밖의 색상 견본을 선택하면 두 개의 밝은 영역이 표시됩니다.
   * 자동 스크롤 `selectSwatch()` 메서드가 잘못 작동합니다.

* VideoPlayer

   * 대체(fallback)가 자동으로 설정되어 있으므로 찾기가 100%로 설정된 경우 비디오 프레임이 업데이트되지 않습니다.
   * Chrome, Firefox 및 Internet Explorer 브라우저의 HLS 스트리밍 모드에서 비디오 검색 중에 비디오 찾기가 차단될 수 있습니다.
   * 처음 방문자가 Microsoft® Edge 브라우저에 포스터 이미지가 표시되지 않을 수 있습니다.
   * 점진적 재생이 사용될 때 Internet Explorer 9에서 비디오가 로드된 후 포스터 이미지가 숨겨질 수 있습니다.

## Dynamic Media Image Serving 6.3.2 및 Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC 유틸리티 - `downsample2x2` 플래그가 더 이상 지원되지 않습니다. 이 플래그는 더 이상 IPS에 사용되지 않는 품질이 낮은 2x2 다운샘플러 입니다.
* CORS 헤더 - 현재, CORS 헤더가 `/is/content/` 요청.
