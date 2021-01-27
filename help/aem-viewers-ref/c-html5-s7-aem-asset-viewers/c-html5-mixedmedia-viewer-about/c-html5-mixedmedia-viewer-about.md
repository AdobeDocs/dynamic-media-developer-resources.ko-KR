---
description: 혼합 미디어 뷰어는 미디어 뷰어입니다. 이미지, 견본 집합, 스핀 집합, 비디오 및 응용 비디오 집합이 포함된 미디어 집합을 지원합니다.
keywords: responsive
solution: Experience Manager
title: 혼합 미디어
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '2660'
ht-degree: 0%

---


# 혼합 미디어{#mixed-media}

혼합 미디어 뷰어는 미디어 뷰어입니다. 이미지, 견본 집합, 스핀 집합, 비디오 및 응용 비디오 집합이 포함된 미디어 집합을 지원합니다.

뷰어 아래쪽에 있는 축소판은 각 미디어 세트 요소와 해당 에셋 유형 표시기를 나타냅니다. 견본 집합 요소를 선택하면 견본 집합 내에서 색상 변형을 선택할 수 있도록 견본의 보조 행이 나타납니다. 이미지 및 견본 집합 요소는 연속 또는 인라인 모드에서 확대/축소를 지원합니다.회전 집합은 확대/축소 및 회전을 모두 지원합니다. 비디오 내용 위에 선택 사항으로 닫힌 캡션이 표시되는 한 비디오 및 응용 비디오 세트는 모든 기본 재생 컨트롤을 지원합니다. 사용자는 언제든지 전체 화면 버튼을 클릭하여 전체 화면으로 전환할 수 있습니다. 뷰어에는 선택 사항으로 닫기 단추가 있습니다. 데스크탑과 모바일 디바이스에서 작동하도록 설계되었습니다.

혼합 미디어 뷰어는 기본 시스템에서 HTML5 스트리밍 비디오 재생을 지원할 때마다 기본 구성에서 HLS 형식으로 사용합니다. HTML5 스트리밍을 지원하지 않는 시스템에서 뷰어는 HTML5 점진적 비디오 전달으로 돌아갑니다.

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형 505.

[시스템 요구 사항 및 사전 요구 사항](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)을 참조하십시오.

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## 혼합 미디어 뷰어 사용 {#section-f21ac23d3f6449ad9765588d69584772}

혼합 미디어 뷰어는 뷰어가 런타임에 다운로드한 기본 JavaScript 파일과 도우미 파일 집합(단일 JavaScript는 이 특정 뷰어에서 사용하는 모든 뷰어 SDK 구성 요소, 자산, CSS)을 나타냅니다.

IS-뷰어와 함께 제공된 프로덕션 준비 HTML 페이지를 사용하여 혼합 미디어 뷰어를 팝업 모드에서 사용할 수 있습니다. 또는 포함된 모드에서 뷰어를 사용할 수 있습니다. 이 모드에서는 문서화된 API를 사용하여 대상 웹 페이지에 연결됩니다.

뷰어를 구성하고 스킨하는 작업은 다른 뷰어와 유사합니다. 모든 스키닝은 사용자 지정 CSS를 통해 수행됩니다.

모든 뷰어에 공통되는 [명령 참조 - 모든 뷰어에 공통되는 구성 특성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [명령 참조 - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 혼합 미디어 뷰어와 상호 작용 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

혼합 미디어 뷰어는 다른 모바일 응용 프로그램에서 일반적으로 사용되는 단일 터치 및 다중 터치 제스처를 지원합니다. 뷰어가 사용자의 스와이프 동작을 처리할 수 없는 경우 웹 브라우저로 이벤트를 전달하여 기본 페이지 스크롤을 수행합니다. 이 기능을 사용하면 뷰어가 장치 화면 영역의 대부분을 차지하는 경우에도 페이지를 탐색할 수 있습니다.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>제스처 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>한 번의 탭 </p> </td> 
   <td colname="col2"> <p> 플라이아웃 보기를 활성화하거나 기본 및 보조 확대/축소 수준 사이의 변경을 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>두 번 누르기 </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 연속 </span> 확대/축소 모드에서 최대 배율에 도달할 때까지 한 수준 확대하면 다음 두 번 누르기 동작은 초기 상태로 재설정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>길게 터치하기 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 인라인 </span> 확대/축소 모드에서는 확대된 이미지를 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>핀치 </p> </td> 
   <td colname="col2"> <p>연속 확대/축소 모드에서는 이미지를 확대하거나 축소합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>가로로 스와이프 또는 튀김 </p> </td> 
   <td colname="col2"> <p> 현재 에셋이 스핀 세트인 경우 이미지가 다시 설정된 상태이면 회전 집합을 가로로 회전합니다. </p> <p> 현재 에셋이 스핀 세트 또는 이미지인 경우 이미지를 확대하면 이미지가 가로로 이동합니다. 이미지가 보기 가장자리로 이동되고 스와이프가 해당 방향으로 계속 수행되면 제스처는 기본 페이지 스크롤을 수행합니다. </p> <p> 견본 막대에서 견본 목록을 스크롤합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세로 손가락 대기 또는 뒤틀기 </p> </td> 
   <td colname="col2"> <p> 이미지가 재설정 상태인 경우 다차원 회전 집합을 사용할 경우 세로 보기 각도가 변경됩니다. 1차원 회전 집합에서 또는 다차원 회전 집합이 마지막 또는 첫 번째 축에 있는 경우 세로 스와이프로 인해 수직 보기 각도가 변경되지 않도록 제스처는 기본 페이지 스크롤을 수행합니다. </p> <p> 현재 에셋이 스핀 세트 또는 이미지이고 이미지를 확대하면 이미지를 세로로 이동합니다. 이미지가 보기 가장자리로 이동되고 스와이프가 해당 방향으로 계속 수행되면 제스처는 기본 페이지 스크롤을 수행합니다. </p> <p> 제스처가 견본 영역 내에서 수행되면 기본 페이지 스크롤이 수행됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

또한 뷰어는 터치 스크린과 마우스로 Windows 장치에서 터치 입력 및 마우스 입력을 모두 지원합니다. 그러나 이러한 지원은 Chrome, Internet Explorer 11 및 Edge 웹 브라우저에만 제한됩니다.

이 뷰어는 키보드로 완벽하게 액세스할 수 있습니다.

[키보드 액세스 가능성 및 탐색](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)을 참조하십시오.

## 혼합 미디어 뷰어 {#section-6bb5d3c502544ad18a58eafe12a13435} 포함

웹 페이지마다 뷰어 비헤이비어에 대한 요구 사항이 다릅니다. 웹 페이지가 클릭했을 때 별도의 브라우저 창에서 뷰어를 여는 링크를 제공하는 경우가 있습니다. 다른 경우에는 호스팅 페이지에 뷰어를 바로 포함해야 합니다. 후자의 경우, 웹 페이지에 정적 페이지 레이아웃이 있거나, 다른 장치 또는 다른 브라우저 창 크기에 대해 다르게 표시되는 응답형 디자인을 사용할 수 있습니다. 이러한 요구 사항을 수용하기 위해 뷰어는 3가지 기본 작업 모드를 지원합니다.팝업, 고정 크기 임베드 및 반응형 디자인 임베드.

## 팝업 모드 {#section-77d5aa03b8b94566958a179b1a2cd474} 정보

팝업 모드에서 뷰어는 별도의 웹 브라우저 창이나 탭에서 열립니다. 브라우저 크기가 조정되거나 모바일 장치의 방향이 변경될 때 브라우저 창 전체 영역이 표시되고 조정됩니다.

팝업 모드는 모바일 장치에서 가장 일반적으로 사용됩니다. 웹 페이지는 `window.open()` JavaScript 호출, 적절히 구성된 `A` HTML 요소 또는 기타 적절한 방법을 사용하여 뷰어를 로드합니다.

팝업 작업 모드에 기본 HTML 페이지를 사용하는 것이 좋습니다. 이 경우 이 이름은 [!DNL MixedMediaViewer.html]이며 표준 IS-Viewers 배포의 [!DNL html5/] 하위 폴더 내에 있습니다.

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

사용자 지정 CSS를 적용하여 시각적 사용자 지정을 실현할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## 고정 크기 및 반응형 디자인 임베드 정보 {#section-ec86b100ba5943d0b16694268520bbde}

포함된 모드에서 뷰어는 기존 웹 페이지에 추가되며, 이 페이지에 이미 뷰어와 관련이 없는 일부 고객 컨텐츠가 있을 수 있습니다. 뷰어는 보통 웹 페이지의 부동산 중 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치의 웹 페이지 지향 및 장치 유형에 따라 자동으로 레이아웃을 조정하는 반응형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 크기 임베딩이 사용됩니다. 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 임베드는 뷰어의 컨테이너 `DIV`의 크기 변경에 응답하여 런타임에 뷰어 크기를 조정해야 할 수 있다고 가정합니다. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

반응형 디자인 임베드 모드에서 뷰어는 웹 페이지의 컨테이너 크기 `DIV`에 따라 다르게 동작합니다. 웹 페이지가 `DIV` 컨테이너의 너비만 설정하고 높이를 제한하지 않은 경우 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능을 사용하면 측면 패딩 없이 에셋이 보기에 완벽하게 맞춰집니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 디자인 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적으로 사용됩니다.

그렇지 않은 경우 웹 페이지가 뷰어의 컨테이너 `DIV`에 대한 폭과 높이를 모두 설정하는 경우 뷰어는 해당 영역만 채우고 웹 페이지 레이아웃이 제공하는 크기를 따릅니다. 예를 들어 뷰어를 모달 오버레이에 포함시켜 오버레이의 크기가 웹 브라우저 창 크기에 따라 조정됩니다.

## 고정 크기 포함 {#section-17d162f76ffa4804b27928f51e7bea1d}

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. `DIV` 컨테이너를 정의합니다.
1. 뷰어 크기를 설정합니다.
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 [!DNL MixedMediaViewer.js]을(를) 포함해야 합니다. [!DNL MixedMediaViewer.js] 파일은 표준 IS-Viewers 배포의 [!DNL html5/js/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

뷰어가 Adobe Dynamic Media Classic 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-Viewers가 설치된 Adobe Dynamic Media Classic 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
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
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 뷰어 크기 설정

   이 뷰어는 다중 항목 세트로 작업할 때 축소판을 표시합니다. 데스크탑 시스템에서 축소판은 기본 보기 아래에 표시됩니다. 동시에 뷰어는 `setAsset()` API를 사용하여 런타임 중에 기본 에셋을 교환하도록 허용합니다. 개발자는 새 에셋에 항목이 하나만 있을 때 뷰어가 맨 아래에 있는 축소판 영역을 관리하는 방법을 제어할 수 있습니다. 외부 뷰어 크기를 그대로 유지하면서 기본 보기의 높이가 증가하여 축소판 영역을 차지하도록 할 수 있습니다. 또는 기본 보기 크기를 정적으로 유지하거나 외부 뷰어 영역을 축소하여 웹 페이지 콘텐츠를 위로 이동한 다음 축소판에서 남은 무료 페이지 공간을 사용할 수 있습니다.

   외부 뷰어 경계를 그대로 유지하려면 `.s7mixedmediaviewer` 최상위 CSS 클래스의 크기를 절대 단위로 정의합니다. CSS의 크기 조정은 HTML 페이지 또는 나중에 Dynamic Media Classic의 뷰어 사전 설정 레코드에 할당되거나 스타일 명령을 사용하여 명시적으로 전달된 사용자 정의 뷰어 CSS 파일에서 바로 적용될 수 있습니다.

   뷰어를 CSS로 스타일링하는 방법에 대한 자세한 내용은 [혼합 미디어 뷰어 사용자 지정](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4)을 참조하십시오.

   다음은 HTML 페이지에서 정적 외부 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음 샘플 페이지에서 고정된 외부 뷰어 영역을 사용하는 동작을 볼 수 있습니다. 세트 간에 전환할 때 외부 뷰어 크기는 변경되지 않습니다.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   기본 보기 차원을 정적으로 만들려면 `.s7mixedmediaviewer .s7container` CSS 선택기를 사용하거나 `stagesize` 수정자를 사용하여 내부 `Container` SDK 구성 요소의 절대 단위로 뷰어 크기를 정의합니다.

   다음은 에셋을 전환할 때 기본 보기 영역의 크기가 변경되지 않도록 내부 `Container` SDK 구성 요소의 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   다음 샘플 페이지에서는 기본 보기 크기가 고정된 뷰어 동작을 보여 줍니다. 세트 간에 전환할 때 기본 보기는 정적 상태로 유지되며 웹 페이지 내용은 세로로 이동됩니다.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   다음과 같이 Dynamic Media Classic의 뷰어 사전 설정 레코드에 `stagesize` 수정자를 설정하거나, 뷰어 초기화 코드를 `params` 컬렉션으로 명시적으로 전달하거나, 이 도움말의 명령 참조 섹션에 설명된 대로 API 호출로 전달할 수 있습니다.

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   CSS 기반 접근 방식이 권장되며 이 예에서 사용됩니다.

1. 뷰어를 만들고 초기화합니다.

   위의 단계를 완료하면 `s7viewers.MixedMediaViewer` 클래스의 인스턴스를 만들고 모든 구성 정보를 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 생성자에게 JSON 개체로 전달됩니다. 적어도 이 개체에는 뷰어가 지원하는 구성 매개 변수를 사용하여 뷰어 컨테이너 ID의 이름을 유지하고 중첩된 `params` JSON 개체가 있는 `containerId` 필드가 있어야 합니다. 이 경우 `params` 객체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL, `videoserverurl` 속성으로 전달된 비디오 서버 URL 및 `asset` 매개 변수로 초기 에셋이 있어야 합니다. JSON 기반 초기화 API를 사용하여 단일 코드 행을 사용하여 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 최대 호환성을 위해 닫는 `BODY` 태그 바로 앞 또는 본문 `onload()` 이벤트에서 `init()` 메서드를 호출합니다.

   이와 동시에 컨테이너 요소가 웹 페이지 레이아웃에 반드시 포함되어야 하는 것은 아닙니다. 예를 들어, 지정된 `display:none` 스타일을 사용하여 숨겨질 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 지연합니다. 이 경우 뷰어 부하가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 예제입니다. 이 예제에서는 `mixedMediaViewer`이(가) 뷰어 인스턴스라고 가정합니다.`s7viewer`은 자리 표시자 `DIV`;의 이름입니다.[!DNL http://s7d1.scene7.com/is/image/]은(는) 이미지 제공 URL입니다.[!DNL http://s7d1.scene7.com/is/content/]은(는) 비디오 서버 URL입니다.및 [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample]은(는) 자산입니다.

```
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

다음 코드는 크기가 고정된 혼합 미디어 뷰어를 포함하는 간단한 웹 페이지의 완전한 예입니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 무제한 높이가 {#section-056cb574713c4d07be6d07cf3c598839}인 응답형 포함

반응형 디자인 임베딩을 사용하면 일반적으로 웹 페이지에는 뷰어의 컨테이너 `DIV`의 런타임 크기를 지정하는 유연한 레이아웃이 있습니다. 다음 예를 들어 웹 페이지에서 뷰어의 컨테이너 `DIV`에 웹 브라우저 창 크기의 40%를 사용할 수 있으며 높이는 제한이 없다고 가정합니다. 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 임베드 단계와 유사합니다. 유일한 차이점은 뷰어 크기를 명시적으로 정의할 필요가 없다는 것입니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. 컨테이너 DIV를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 임베딩과 동일합니다. 기존 `"holder"` DIV에 컨테이너 DIV를 추가합니다. 다음 코드는 완전한 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 변경되는 방법과 뷰어 종횡비가 에셋과 일치하는 방식을 확인합니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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

## 너비 및 높이가 정의된 유연한 크기 포함 {#section-0a329016f9414d199039776645c693de}

폭 및 높이가 정의된 유연한 크기를 포함하는 경우 웹 페이지 스타일이 다릅니다. 이 도구는 `"holder"` DIV에 두 크기를 모두 제공하고 브라우저 창에 정렬합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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

나머지 포함 단계는 높이가 제한되지 않은 응답형 디자인 임베드에 사용되는 단계와 동일합니다. 결과 예는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Setter 기반 API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}를 사용하여 포함

JSON 기반 초기화를 사용하는 대신 setter 기반 API 및 인수 없음 생성자를 사용할 수 있습니다. 이 API 생성자를 사용해도 매개 변수와 구성 매개 변수는 별도의 JavaScript 호출과 함께 `setContainerId()`, `setParam()` 및 `setAsset()` API 메서드를 사용하여 지정되지 않습니다.

다음 예제에서는 setter 기반 API와 함께 고정 크기 임베드를 사용하는 방법을 보여 줍니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```

