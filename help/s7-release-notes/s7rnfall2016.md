---
title: Scene7 2016년 가을 릴리스
description: "Adobe Experience Cloud의 Adobe Experience Manager 솔루션의 일부인 Adobe Scene7 2016년 가을 릴리스의 최신 릴리스 정보입니다."
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2236'
ht-degree: 0%

---

# Scene7 2016년 가을 릴리스{#scene-fall-release}

Adobe Experience Cloud에 있는 Adobe Scene7 Adobe Experience Manager 솔루션의 2016년 가을 릴리스 부분에 대한 최신 릴리스 정보입니다.

## Scene7 2016년 가을 릴리스 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

[!DNL Adobe Experience Cloud]에 있는 [!DNL Adobe Experience Manager] 솔루션의 [!DNL Adobe Scene7] 2016년 가을 릴리스 부분에 대한 최신 릴리스 정보입니다.

* [일반](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [뷰어(이미지 제공 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [뷰어(이미지 제공 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [뷰어(이미지 제공 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 뷰어 SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic 이미지 제공 6.3.2 및 이미지 렌더링 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 일반 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe은 전반적인 성능이 개선된 HTTP/2 컨텐츠 제공을 발표하게 됩니다.

[HTTP2 콘텐츠 배달 FAQ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic)를 참조하십시오.

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

전체 문서를 보려면 [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)을(를) 참조하십시오.

**새로운 기능, 개선 사항 및 버그 수정**

* [!DNL Adobe Scene7 Publishing System] 사용자 인터페이스에서 비디오 다시 자르기 기능을 제거했습니다.
* 필요하고 가능한 경우 모든 Scene7 서블릿에 인증이 추가되었습니다
* 휴지통의 목록 보기와 관련된 버그 수정.
* 보안 문제로 인해 사용자 관리에서 **Dynamic Media Classic(Scene7) 관리자 만들기** 사용자 기능을 제거했습니다.
* FTP WebAdmin이 이제 OKTA 인증을 지원합니다.
* 새 Media Portal 사용자에 대해 생성된 기본 암호 기능을 제거했습니다.
* 새 사용자가 추가되었을 때 생성된 임시 암호와 관련된 버그 수정. 암호가 필요한 암호 요구 사항을 충족하지 않았습니다.
* WebAdmin 루트 디스크가 꽉 찬 문제가 해결되었습니다.
* 사용자 비활성화 관련 버그 수정이 사용자 인터페이스에 즉시 반영되지 않습니다.
* 나중에 사용자를 다시 만들 수 없었던 사용자 삭제와 관련된 버그 수정.
* 특정 설정을 제어하는 인증을 포함하지 않은 새 Scene7 사용자에게 전송된 시작 이메일과 관련된 버그 수정.
* 이름에 특수 문자가 있는 폴더가 있을 경우 FTP 폴더 목록을 검색하지 못한 것과 관련된 버그 수정입니다.
* Scene7 환경에 대한 OKTA 서비스 공급자를 구성합니다.
* Viewer Analytics에 대한 Experience Cloud 조직 ID에 대한 지원이 추가되었습니다.
* Scene7 SAML 소비자를 구현했습니다.

## 뷰어(이미지 제공 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

전체 문서를 보려면 [뷰어 참조 안내서](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en)를 참조하십시오.

**이미지 제공 5.5.3에 대한 버그 수정**

* RequireJS 및 DOJO 라이브러리와의 호환성.

  뷰어 배포 중 통합 SDK JS 캐싱.

## 뷰어(이미지 제공 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

전체 문서를 보려면 [뷰어 참조 안내서](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en)를 참조하십시오.

**이미지 제공 5.5.2에 대한 버그 수정**

* Windows 7의 Internet Explorer 11에서 비디오를 재생하지 못했습니다.
* `initialframe`이(가) HTML5 eCatalog용 모바일 장치의 세로 모드에 영향을 주지 않았습니다.

## 뷰어(이미지 제공 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

전체 문서를 보려면 [뷰어 참조 안내서](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en)를 참조하십시오.

**이미지 제공 5.5.1에 대한 새로운 기능, 개선 사항 및 버그 수정**

* 검색 기능이 있는 HTML 5 eCatalog 뷰어입니다.
* 대부분의 데스크탑 시스템에 대한 기본 비디오 제공 방법으로 HLS 스트리밍 비디오 재생을 추가했습니다. Flash 기반 HDS 비디오 스트리밍은 여전히 대체 재생 옵션으로 사용할 수 있습니다.
* Chrome 브라우저를 실행하는 마우스와 터치 입력이 모두 있는 장치에 대한 지원을 추가했습니다.
* Analytics 통합에 Experience Cloud 조직 ID 지원이 추가되었습니다.
* AppMeasurement JavaScript 라이브러리를 버전 1.6.1로 업데이트합니다.
* eCatalog 뷰어에 오른쪽에서 왼쪽 방향 지원이 추가되었습니다.
* `tip=0,-1,0`에서 범위를 벗어나는 오류가 발생하던 문제를 해결했습니다.

**호환성 정보**

* 블랙베리®

   * 이전 AVS 세트와 호환되지 않습니다. 재생을 허용하려면 클라이언트가 AVS 세트를 다시 업로드해야 합니다.

* 일반

   * 브라우저 쪽 크기 조절로 인해 사용자가 페이지를 확대하면 UI 및 이미지가 흐릿해질 수 있습니다. UI 서식은 확대/축소에 따라 잘못 표시될 수도 있습니다. 이 효과는 전체 화면으로 이어집니다.
   * 모바일 장치의 크기 제한으로 인해 혼합 미디어 뷰어는 슬라이드 제스처를 사용하여 포함된 견본 구성 요소를 탭하는 대신 포함된 이미지 세트의 프레임을 전환합니다. 구성 요소가 시각적 표시기로 표시됩니다.
   * Internet Explorer 브라우저 및 일부 터치 장치에서 전체 화면 모드는 전체 장치 화면을 차지하지 않습니다. 대신 브라우저 창의 크기로 응용 프로그램의 크기를 조정합니다.
   * 닫기 버튼은 iOS 8.0 및 8.1에서 작동하지 않지만 iOS 8.2에서는 더 이상 작동하지 않습니다

* 갤럭시

   * Zoom 및 eCatalog HTML5 뷰어에서 메모리 누수가 확인되었습니다. 프레임을 통해 반복적으로 탐색하면 브라우저가 충돌할 수 있습니다.
   * 뷰어를 두 번 탭하면 브라우저 쪽 확장이 활성화된 뷰어가 아닌 전체 페이지가 확대/축소될 수 있습니다.

* 갤럭시

   * 브라우저 설정에서 전체 화면을 확인한 상태로 장치가 세로 모드에서 태블릿으로 감지되었습니다.

* 갤럭시 넥서스

   * 뷰어를 두 번 탭하면 브라우저 쪽 확장이 활성화된 뷰어가 아닌 전체 페이지가 확대/축소될 수 있습니다.

* Galaxy Nexus 10 및 갤럭시 태블릿

   * 세로 및 가로 방향의 잘못된 페이지 스프레드를 표시하는 전자 카탈로그입니다.

* HTC 모바일 장치

   * HTC 모바일 장치 Adobe의 결과는 기본 핀치 확대/축소를 비활성화할 수 없음이 HTC UI 래퍼 (HTC 센스)의 &quot;기능&quot;임을 보여줍니다. 이 문제로 인해 뷰어에서 &quot;핀치 투 줌&quot; 제스처를 사용할 때 전체 페이지가 확대/축소될 수 있습니다. 대신 두 번 탭하여 사용하는 것이 좋습니다.
   * 이미지 맵 아이콘들은 이미지 맵들이 작고 함께 닫혀 있는 경우 중첩될 수 있다.

* HTML5 비디오

   * Internet Explorer 9: 사용자 지정 포스터 이미지가 표시되지 않습니다.
   * `IntialBitRate` 수정자는 소프트웨어 HLS 및 Flash HDS 재생에서만 지원됩니다. 재생이 기본 플레이어를 사용하는 경우 작동하지 않습니다.
   * OGG 및 WebM 점진적 재생은 현재 지원되지 않습니다.
   * 브라우저 크기 조정으로 인해 비디오 플레이어가 잘못된 크기로 표시될 수 있습니다(Windows OS 제어판 표시 설정 포함).
   * Safari에서 HLS 스트리밍을 사용하는 비디오 찾기가 일관되지 않을 수 있습니다.

* Internet Explorer

   * Quirks 모드는 현재 지원되지 않습니다.
   * 호환 모드는 현재 지원되지 않습니다.
   * 모바일의 Internet Explorer는 현재 지원되지 않습니다.

* iOS

   * 큰 eCatalogs는 iPad 2에서 브라우저 충돌을 일으킬 수 있습니다.
   * iPhone 6+ 휴대폰은 시청자에 의해 태블릿으로 감지됩니다.

* Safari

   * Safari 6.1 이상: 인터넷 플러그인 설정으로 인해 Flash 비디오가 재생되지 않을 수 있습니다.
   * Safari에서 HLS 스트리밍을 사용하는 비디오 &quot;찾기&quot;가 일관되지 않을 수 있습니다.
   * HLS 스트리밍을 사용하여 Safari 6에서 비디오의 끝을 찾을 수 없습니다.

**알려진 문제 및 제한 사항**

* `iscommands`의 이미지 제공 수정자가 `req=set` 요청에 기본적으로 추가되지 않습니다. 이미지 표시에만 영향을 주는 수정자가 제대로 작동합니다. 크기에 영향을 주는 수정자는 복잡한 에셋에서 사용해야 합니다. 예:

  `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [플라이아웃] IE9은 마우스가 꺼진 후에도 화면에 남아 있는 경우가 있습니다.
* 브라우저 크기 조정으로 인해 크기를 잘못 조정할 수 있습니다.
* iPad 2: 대형 eCatalog 자산이 iOS에서 Safari를 충돌시킵니다.
* 모든 뷰어

   * 워터마크, 난독화 및 잠금은 지원되지 않습니다.
   * 이미지 사전 설정은 지원되지 않습니다.
   * `display:none` CSS를 사용하거나 부모 노드에서 동적으로 분리하여 DOM에서 뷰어를 추가하거나 제거하는 작업은 현재 지원되지 않습니다.

* HTML5 모든 뷰어

   * 뷰어를 테이블에 포함시키면 기본 전체 화면 모드가 아닌 뷰어의 크기 조정이나 배치가 잘못될 수 있습니다. 대신 DIV를 사용하는 것이 좋습니다.
   * 코드에서 명시적 인스턴스 이름이 있는 매개 변수는 URL의 인스턴스 이름뿐만 아니라 덮어써야 합니다(예: `zoomView.iconfeffect=0`).
   * 이미지 제공 명령 자르기는 현재 지원되지 않습니다.
   * 닫기 단추는 뷰어가 하위 창에 열려 있는 경우에만 작동합니다.
   * `iscommands` 한정자는 이미지 크기에 영향을 주는 이미지 제공 한정자를 지원하지 않습니다.

* HTML5 eCatalog

   * 다른 HTML 페이지로 이동한 다음 다시 돌아가는 경우 뷰어가 다시 첫 번째 페이지로 재설정됩니다.
   * iOS 디바이스를 회전한 후 페이지 레이아웃이 잘못 표시되는 경우가 있습니다. 페이지 확대/축소는 레이아웃을 수정합니다.
   * 내부 링크는 다중 페이지 스프레드에서 맨 왼쪽 페이지에만 연결됩니다. 세로 모드에서 모바일 장치에 영향을 줍니다.
   * InitalFrame은 여러 페이지 스프레드에서 맨 왼쪽 페이지에만 연결됩니다. 세로 모드에서 모바일 장치에 영향을 줍니다.
   * 브라우저 제한 사항으로 인해 IE9에서는 인쇄 기능을 사용할 수 없습니다.

* HTML5 MixedMedia

   * 사운드트랙 재생은 지원되지 않습니다.

* HTML5 소셜

   * 발신 이메일에서 썸네일을 제대로 렌더링하려면 `serverurl` 한정자에 절대 URL이 있어야 합니다.

* HTML5 비디오

   * 포스터 이미지에 &quot;최대 크기&quot; 오류가 발생할 수 있습니다. 회사는 이미지 제공 Publish에 대한 제한 설정을 늘려야 합니다.
   * HTML 페이지 호스팅이 외부 서버(Scene7 서버 아님)에서 제공되는 경우 비디오 캡션에는 회사 규칙 세트가 필요합니다. 도움이 필요하면 Adobe 지원 센터에 문의하십시오.
   * Analytics 추적에서 버퍼링으로 인해 잘못된 재생 비율이 보고될 수 있음
   * 포스터 이미지 대신 검정색 프레임이 iPad 또는 Android™ 디바이스에 표시될 수 있습니다.
   * iPad 또는 Android™ 장치에서 뷰어를 로드하는 동안 화면에서 검은색 프레임이 깜박일 수 있습니다.
   * iPad 장치에서 배경을 흰색/투명으로 설정하면 VideoPlayer 구성 요소 옆에 검정색 테두리가 표시됩니다.
   * iOS 7을 사용하여 비디오의 마지막 프레임이 iPad에서 왜곡될 수 있습니다.
   * Chrome, Firefox 및 Internet Explorer 브라우저의 HLS 스트리밍 모드에서 비디오 검색 중에 가끔 매크로차단이 발생할 수 있습니다.
      * 포스터 이미지가 Microsoft® Edge 브라우저에 처음 표시되지 않을 수 있습니다.
      * 포스터 이미지는 점진적 재생을 사용할 때 Internet Explorer 9에서 비디오 로드 후 숨겨질 수 있습니다.

## Scene7 HTML5 뷰어 SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

사용 안내서는 클라이언트 설치의 Adobe HTML5 Viewer SDK 폴더에 있습니다. 구성 요소 API 설명서는 클라이언트 설치의 docs 하위 폴더에 있습니다.

**3.0.2에 대한 버그 수정**

* VideoPlayer - Windows 7의 Internet Explorer 11에서 비디오를 재생하지 못했습니다.
* TableOfContents - `initialframe`이(가) HTML 5 eCatalog 뷰어의 모바일 장치에서 세로 모드에 영향을 주지 않았습니다.

**3.0.1에 대한 새로운 기능, 개선 사항 및 버그 수정**

* 일반

   * 대부분의 데스크탑 시스템에 대한 기본 비디오 제공 방법으로 HLS 스트리밍 비디오 재생을 추가했습니다. Flash 기반 HDS 비디오 스트리밍은 여전히 대체 재생 옵션으로 사용할 수 있습니다.
   * eCatalog 뷰어의 새 검색 기능을 지원하기 위해 SearchManager, SearchPanel, SearchEffect 및 SearchButton 구성 요소를 추가했습니다.
   * Chrome 브라우저에서 마우스와 터치 입력이 모두 실행되는 장치에 대한 지원이 추가되었습니다.
   * 향후 버전의 OS를 지원하도록 Android™ 버전 감지 를 리팩터링했습니다.
   * eCatalog별 SDK 구성 요소에 오른쪽에서 왼쪽 방향 지원을 추가합니다.

* 컨트롤 막대

   * ControlBar 콘텐츠가 사용 가능한 너비에 맞지 않을 경우에 대비해 선택적 스크롤링을 추가했습니다.

* 플라이아웃확대/축소 보기

   * `tip=0,-1,0`이(가) 범위를 벗어나는 오류를 일으킨 사례를 수정했습니다.

**호환성 정보**

* Android™ 4.x

   * 기본값을 비활성화하려면 구성 요소에 대해 다음 CSS 규칙을 파란색 강조 표시로 추가해야 합니다.

     `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* 블랙베리®

   * AVS 세트들에서 비트 레이트 스트림들을 변경할 때 비디오 재생이 중단될 수도 있다.

* Chrome

   * Chrome의 내부 캐싱으로 인해 구성 요소를 다시 빌드하도록 하는 모든 API 호출은 무시될 수 있습니다.

* 갤럭시

   * 뷰어가 전체 화면으로 로드되지 않는 경우가 있습니다.
   * Pageview에서 현재 장치의 메모리 누수가 발생합니다.
   * 브라우저 쪽 크기 조절을 활성화하면 두 번 누르기 제스처가 뷰어와 페이지를 확대합니다.

* 갤럭시 넥서스

   * 일부 보기 구성 요소에 표시되는 아티팩트.
   * 브라우저 쪽 크기 조절을 활성화하면 두 번 누르기 제스처가 뷰어와 페이지를 확대합니다.

* IPAD 3

   * iPad 3의 기본 해상도는 2048x1536입니다. 이 해결 방법은 회사의 IS가 게시되고 이미지 크기 제한이 더 낮게 설정된 경우 표시 문제를 일으킬 수 있습니다.

* iPhone

   * 페이지를 스크롤한 후 Iconeffect 재생 아이콘이 재생 아이콘으로 대체되었습니다.

* Internet Explorer

   * IE 10 및 이전의 전체 화면 모드는 전체 화면을 차지하지 않고 브라우저 창의 크기로 응용 프로그램의 크기를 조정합니다.
   * Quirks 렌더링 모드는 지원되지 않습니다.
   * 모바일의 Internet Explorer는 현재 지원되지 않습니다.
   * 비동기식으로 포함된 경우 Util.js가 로드되지 않을 수 있습니다.
   * IconEffect 아이콘은 SpinView 및 ZoomView 구성 요소에서 클릭 이벤트를 차단합니다.

* 기본 장치 비디오 플레이어

   * VideoPlayer를 사용하여 장치의 기본 플레이어를 호출하는 경우 VideoPlayer를 통한 UI 구성 요소 계층화는 지원되지 않습니다.
   * 기본 모드에서 비디오 재생이 Safari 6에서 일관되지 않습니다.
   * 기본 재생은 페이지를 스크롤한 후 재생 아이콘을 재생 아이콘으로 대체합니다.

* 터치 장치

   * 전체 화면 모드는 전체 장치 화면을 차지하지 않고 브라우저 창의 크기로 응용 프로그램 크기를 조정합니다.
   * 터치 장치에서는 사용자 지정 커서가 작동하지 않습니다.
   * 터치 장치에서의 페이지 확대는 현재 지원되지 않습니다. HTML5 뷰어를 포함하려면 적절한 설정이 있는 뷰포트 메타 태그가 필요합니다.

* Xom

   * 브라우저 쪽 크기 조절을 활성화하면 두 번 누르기 제스처가 뷰어와 페이지를 확대합니다.

**알려진 문제 및 제한 사항**

* 모든 구성 요소

   * 버전 2.7.2 및 이전 버전에서는 일부 구성 요소가 `insertBefore()` API를 사용하여 DOM에 추가되었습니다. 따라서 구성 요소 인스턴스가 다른 구성 요소에 대해 만들어지는 경우와 상관없이 이러한 구성 요소는 자신을 스택 순서의 맨 아래에 놓습니다. 2.8.1 릴리스에서는 모든 구성 요소가 `appendChild()` API를 사용하고 있습니다. 즉, 구성 요소 스택 순서가 인스턴스 생성 순서와 일치합니다.

   * `iscommand` 수정자를 사용하여 이미지 알파 채널 형식을 설정할 수 없습니다. 대신 구성 요소 `FMT` 매개 변수를 사용하십시오.
   * CSS 변형 속성은 현재 지원되지 않습니다.

* 터치 장치

   * 터치 디바이스 상의 핀치 제스처는 줌 이벤트를 생성하지 않는다

* 컨테이너

   * 컨테이너의 테두리, 패딩 및 여백은 지원되지 않습니다. Adobe은 상위 DIV에 스타일 요소를 추가할 것을 제안합니다.
   * 컨테이너 크기를 명시적으로 설정해야 합니다. 그렇지 않으면 구성 요소의 크기가 올바르게 지정될 수 있습니다.

* 인쇄 구성 요소

   * 브라우저 제한 사항으로 인해 Internet Explorer 9에서 인쇄 구성 요소가 용지에 맞게 내용의 크기를 조정하지 못할 수 있습니다.

* IconEffect 구성 요소

   * `autohide`을(를) 사용하지 않도록 설정한 경우(`0`(으)로 설정) IconEffect가 Internet Explorer에서 스크립트 오류를 생성합니다.

* ImageMapEffect 요소

   * 보기 구성 요소에서 이미지를 패닝할 때 아이콘 위치 변경 지연.

* 미디어 집합 구성 요소

   * 인라인 에셋은 URL에서와 동일한 인코딩을 요청합니다.

* 탐색 보기 구성 요소

   * 현재 구성 요소는 크기 변경을 지원하지 않습니다.

* PageScrubber 구성 요소

   * iPhone 5에서 PageScrubber 버블이 텍스트로 설정되면 트랙을 따라 버튼을 슬라이딩 할 때 아티팩트가 표시됩니다. 스타일에서 `-webkit-background-clip: content;`을(를) 사용하면 문제가 해결됩니다.

* SpinView 구성요소

   * 이미지가 회전하는 동안 스와이프 제스처와 디바이스를 회전시킨 후 SpinView가 정지되는 것처럼 보이는 경우가 있습니다.

* 견본 구성 요소

   * 범위를 벗어나는 견본을 선택하면 두 개의 강조 표시가 표시됩니다.
   * `selectSwatch()` 메서드를 사용하여 자동 스크롤하는 작업이 올바르게 작동하지 않습니다.

* VideoPlayer

   * 찾기가 100%로 설정되고 대체가 auto로 설정된 경우 비디오 프레임이 업데이트되지 않습니다.
   * Chrome, Firefox 및 Internet Explorer 브라우저의 HLS 스트리밍 모드에서 비디오 검색 중에 가끔 매크로 차단이 발생할 수 있습니다.
   * 포스터 이미지가 Microsoft® Edge 브라우저에 처음 표시되지 않을 수 있습니다.
   * 포스터 이미지는 점진적 재생을 사용할 때 Internet Explorer 9에서 비디오 로드 후 숨겨질 수 있습니다.

## Dynamic Media 이미지 제공 6.3.2 및 이미지 렌더링 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC 유틸리티 - `downsample2x2` 플래그는 더 이상 지원되지 않습니다. 이 플래그는 더 이상 IPS에서 사용되지 않는 저품질 2x2 다운샘플러였습니다.
* CORS 헤더 - 현재 CORS 헤더가 `/is/content/` 요청에 대해 구성되어 있습니다.
