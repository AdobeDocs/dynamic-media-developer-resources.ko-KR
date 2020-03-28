---
description: eCatalog 검색 뷰어는 스프레드 또는 페이지별로 전자 브로셔를 표시하는 카탈로그 뷰어로서, 사용자는 eCatalog를 사용하여 추가 사용자 인터페이스 요소나 전용 축소판 모드를 사용하여 카탈로그를 탐색할 수 있습니다. 또한 사용자는 모든 페이지를 확대하여 자세히 볼 수 있습니다.
keywords: responsive
seo-description: eCatalog 검색 뷰어는 스프레드 또는 페이지별로 전자 브로셔를 표시하는 카탈로그 뷰어로서, 사용자는 eCatalog를 사용하여 추가 사용자 인터페이스 요소나 전용 축소판 모드를 사용하여 카탈로그를 탐색할 수 있습니다. 또한 사용자는 모든 페이지를 확대하여 자세히 볼 수 있습니다.
seo-title: eCatalog 검색
solution: Experience Manager
title: eCatalog 검색
topic: Dynamic media
uuid: f5ec33bf-e827-4709-9780-6f17096bf306
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# eCatalog 검색{#ecatalog-search}

eCatalog 검색 뷰어는 스프레드 또는 페이지별로 전자 브로셔를 표시하는 카탈로그 뷰어로서, 사용자는 eCatalog를 사용하여 추가 사용자 인터페이스 요소나 전용 축소판 모드를 사용하여 카탈로그를 탐색할 수 있습니다. 또한 사용자는 모든 페이지를 확대하여 자세히 볼 수 있습니다.

이 뷰어는 ecatalog와 연동되며 선택적 이미지 맵 및 소셜 공유 도구를 지원합니다. 확대/축소 툴, 카탈로그 탐색 툴, 전체 화면 지원, 축소판 및 닫기 버튼(선택 사항)이 포함되어 있습니다. 또한 뷰어는 소셜 공유 도구, 인쇄, 다운로드 및 즐겨찾기를 지원합니다. 데스크탑과 모바일 디바이스에서 작동하도록 설계되었습니다.

사용자는 카탈로그 컨텐츠를 키워드 기반 또는 구문 기반 검색으로 수행할 수도 있습니다.

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

뷰어 유형 513.

시스템 [요구 사항 및 전제 조건을 참조하십시오](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 데모 URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/)

## eCatalog 뷰어 사용 {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Search Viewer는 런타임에 뷰어가 다운로드한 기본 JavaScript 파일 및 도우미 파일 집합(단일 JavaScript는 이 특정 뷰어에서 사용하는 모든 뷰어 SDK 구성 요소, 자산, CSS 포함)을 나타냅니다

IS-Viewers와 함께 제공되거나 내장 모드로 제공되는 프로덕션 준비 HTML 페이지를 사용하여 팝업 모드에서 eCatalog Search Viewer를 사용할 수 있습니다. 이 페이지는 문서화된 API를 사용하여 대상 웹 페이지에 통합됩니다.

구성 및 스키닝은 다른 뷰어와 유사합니다. 모든 스키닝은 맞춤형 CSS를 통해 이루어집니다.

모든 [뷰어에 공통으로 사용되는 명령 참조 - 구성 특성](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 및 [모든 뷰어 - URL에 공통되는 명령 참조](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## eCatalog 검색 뷰어와 상호 작용 {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog 검색 뷰어는 다른 모바일 응용 프로그램에서 일반적으로 사용되는 다음 터치 제스처를 지원합니다.

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
   <td colname="col2"> <p> 견본에서 새로운 축소판을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>두 번 누르기 </p> </td> 
   <td colname="col2"> <p> 최대 배율에 도달할 때까지 한 단계 확대합니다. 다음 두 번 누르기 제스처는 뷰어를 초기 보기 상태로 재설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>핀치 </p> </td> 
   <td colname="col2"> <p>확대 또는 축소 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>가로 손가락 대기 또는 깜박임 </p> </td> 
   <td colname="col2"> <p>슬라이드 프레임 전환이 사용되는 경우 카탈로그 페이지 목록을 스크롤합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세로 손가락 대기 또는 깜박임 </p> </td> 
   <td colname="col2"> <p>이미지가 재설정 상태인 경우 기본 페이지 스크롤을 수행합니다. </p> <p>축소판이 활성화되면 축소판 목록이 스크롤됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

카탈로그 페이지 사이를 탐색하는 데 사실적이고 생동감 있는 페이지 뒤집기 애니메이션 효과를 사용할 수 있습니다. 이러한 경우 사용자가 페이지 모서리를 길게 끌거나 페이지를 넘길 수 있습니다.

또한 이 뷰어는 터치 화면과 마우스로 Windows 장치에서 터치 입력 및 마우스 입력을 모두 지원합니다. 그러나 이러한 지원은 Chrome, Internet Explorer 11 및 Edge 웹 브라우저로만 제한됩니다.

## eCatalog 검색 뷰어를 사용한 소셜 미디어 공유 툴 {#section-eb575084a99647c3a9591f439f40b412}

eCatalog Search Viewer는 소셜 공유 도구를 지원합니다. 기본 제어 막대에서 단추를 사용하여 사용자가 클릭하거나 탭하면 공유 도구 모음으로 확장됩니다.

공유 도구 모음에는 Facebook, Twitter, 이메일 공유, 포함 코드 공유 및 링크 공유를 포함하는 지원되는 각 공유 채널 유형에 대한 아이콘이 포함되어 있습니다. 이메일 공유, 포함 공유 또는 링크 공유 도구가 활성화되면 뷰어는 해당 데이터 입력 양식이 있는 모달 대화 상자를 표시합니다. Facebook 또는 Twitter가 호출되면 뷰어는 사용자를 소셜 서비스에서 표준 공유 대화 상자로 리디렉션합니다. 웹 브라우저 보안 제한 때문에 전체 화면 모드에서 공유 도구를 사용할 수 없습니다.

뷰어의 검색 기능은 기본 도구 모음에서 보기 유리 아이콘으로 사용할 수 있습니다. 아이콘을 클릭하거나 탭하면 입력 필드가 있는 검색 패널이 활성화됩니다. 키워드 또는 구문을 입력하고 Enter 키를 누르면 뷰어가 패널에 검색 결과를 렌더링하고 기본 보기에서 찾은 단어를 강조 표시합니다.

## eCatalog 검색 뷰어 포함 {#section-6bb5d3c502544ad18a58eafe12a13435}

웹 페이지마다 뷰어 비헤이비어에 대한 요구 사항이 다릅니다. 경우에 따라 웹 페이지가 클릭하면 별도의 브라우저 창에서 뷰어를 여는 링크를 제공합니다. 다른 경우 호스팅 페이지에 뷰어를 바로 포함해야 합니다. 후자의 경우, 웹 페이지에는 정적 페이지 레이아웃이 있을 수도 있고, 다른 장치 또는 서로 다른 브라우저 창 크기에 대해 다르게 표시되는 반응형 디자인을 사용할 수도 있습니다. 이러한 요구 사항을 충족하기 위해 뷰어는 다음 세 가지 기본 작업 모드를 지원합니다.팝업, 고정 크기 임베드 및 반응형 디자인 임베드.

**팝업 모드 정보**

팝업 모드에서 뷰어는 별도의 웹 브라우저 창이나 탭에서 열립니다. 전체 브라우저 창 영역을 사용하고 브라우저 크기를 조정하거나 모바일 장치의 방향이 변경될 때 조정됩니다.

팝업 모드는 모바일 장치에서 가장 일반적으로 사용됩니다. 웹 페이지는 JavaScript 호출, `window.open()` 적절하게 구성된 HTML `A` 요소 또는 기타 적절한 방법을 사용하여 뷰어를 로드합니다.

팝업 작업 모드에서는 즉시 사용 가능한 HTML 페이지를 사용하는 것이 좋습니다. 이 경우 이 매개 변수를 [!DNL eCatalogSearchViewer.html] 호출하고 표준 IS-뷰어 배포의 [!DNL html5/] 하위 폴더 내에 있습니다.

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

사용자 지정 CSS를 적용하여 시각적 사용자 지정을 수행할 수 있습니다.

다음은 새 창에서 뷰어를 여는 HTML 코드의 예입니다.

```
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**고정 크기 임베드 모드 및 반응형 디자인 임베드 모드 정보**

내장 모드에서 뷰어는 기존 웹 페이지에 추가되며, 여기에는 뷰어와 관련이 없는 일부 고객 컨텐츠가 이미 있을 수 있습니다. 뷰어는 일반적으로 웹 페이지의 부동산의 일부만을 차지합니다.

기본 사용 사례는 데스크톱 또는 태블릿 장치의 웹 페이지 지향 및 장치 유형에 따라 레이아웃을 자동으로 조정하는 반응형 디자인 페이지입니다.

뷰어가 초기 로드 후 크기를 변경하지 않는 경우 크기 임베딩이 사용됩니다. 정적 레이아웃이 있는 웹 페이지에 가장 적합합니다.

반응형 디자인 임베드에서는 컨테이너의 크기 변경에 응답하여 런타임 시 뷰어의 크기를 조정해야 할 수 있다고 가정합니다 `DIV`. 가장 일반적인 사용 사례는 유연한 페이지 레이아웃을 사용하는 웹 페이지에 뷰어를 추가하는 것입니다.

반응형 디자인 임베드 모드에서 뷰어는 웹 페이지의 컨테이너 크기 조절 방식에 따라 다르게 동작합니다 `DIV`. 웹 페이지가 컨테이너의 너비만 설정하고 높이를 제한을 두지 `DIV`않으면 뷰어는 사용되는 자산의 종횡비에 따라 높이를 자동으로 선택합니다. 이 기능을 사용하면 측면에 패딩 없이 에셋이 보기에 완벽하게 맞춰집니다. 이 사용 사례는 Bootstrap, Foundation 등과 같은 반응형 레이아웃 프레임워크를 사용하는 웹 페이지에 가장 일반적으로 사용됩니다.

그렇지 않으면 웹 페이지가 뷰어의 컨테이너 너비와 높이를 모두 설정하는 경우 뷰어는 해당 `DIV`영역만 채우고 웹 페이지 레이아웃이 제공하는 크기를 따릅니다. 예를 들어 뷰어를 모달 오버레이에 포함시켜 오버레이의 크기가 웹 브라우저 창 크기에 따라 조정되는 것이 좋습니다.

**고정 크기 임베드**

다음을 수행하여 웹 페이지에 뷰어를 추가합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. 컨테이너 DIV를 정의합니다.
1. 뷰어 크기 설정
1. 뷰어를 만들고 초기화합니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.

   뷰어를 만들려면 HTML 헤드에 스크립트 태그를 추가해야 합니다. 뷰어 API를 사용하려면 먼저 포함해야 [!DNL eCatalogSearchViewer.js]합니다. 이 [!DNL eCatalogSearchViewer.js] 파일은 표준 IS-뷰어 배포의 [!DNL html5/js/] 하위 폴더 아래에 있습니다.

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

뷰어가 Adobe Scene7 서버 중 하나에 배포되고 동일한 도메인에서 제공되는 경우 상대 경로를 사용할 수 있습니다. 그렇지 않으면 IS-뷰어가 설치된 Adobe Scene7 서버 중 하나에 대한 전체 경로를 지정합니다.

상대 경로는 다음과 같습니다.

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. 컨테이너 DIV를 정의합니다.

   뷰어를 표시할 페이지에 빈 DIV 요소를 추가합니다. DIV 요소에는 이 ID가 나중에 뷰어 API로 전달되므로 ID가 정의되어 있어야 합니다.

   자리 표시자 DIV는 위치 요소입니다. 즉, CSS `position` 속성이 `relative` 또는 `absolute`로 설정되어 있습니다.

   다음은 정의된 자리 표시자 DIV 요소의 예입니다.

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 뷰어 크기 설정

   뷰어의 정적 크기를 절대 단위로 `.s7ecatalogsearchviewer` 최상위 CSS 클래스에 대해 선언하거나 `stagesize` 수정자를 사용하여 설정할 수 있습니다.

   HTML 페이지 또는 사용자 정의 뷰어 CSS 파일에서 바로 크기를 조정할 수 있습니다. 이 파일은 나중에 Scene7 Publishing System의 뷰어 사전 설정 레코드에 할당되거나 스타일 명령을 사용하여 명시적으로 전달됩니다.

   CSS를 [사용하여](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 뷰어의 스타일 지정에 대한 자세한 내용은 eCatalog 뷰어 맞춤화를 참조하십시오.

   다음은 HTML 페이지에서 정적 뷰어 크기를 정의하는 예입니다.

   ```
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Scene7 Publishing System의 뷰어 사전 설정 레코드에서 `stagesize` 수정자를 설정하거나, `params` 컬렉션이 있는 뷰어 초기화 코드와 함께 명시적으로 전달하거나, 명령 참조 섹션에 설명된 대로 API 호출로 전달할 수 있습니다.

   ```
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. 뷰어를 초기화하는 중입니다.

   위의 단계를 완료하면 `s7viewers.eCatalogSearchViewer` 클래스 인스턴스를 만들고 모든 구성 정보를 생성자에 전달하고 뷰어 인스턴스에서 `init()` 메서드를 호출합니다. 구성 정보는 생성자에게 JSON 개체로 전달됩니다. 최소한 이 개체에는 뷰어에서 지원하는 구성 매개 변수를 사용하여 뷰어 컨테이너 ID와 중첩된 `containerId` `params` JSON 개체의 이름이 있는 필드가 있습니다. 이 경우 `params` 개체에는 `serverUrl` 속성으로 전달된 이미지 제공 URL 이상이 있어야 하며 초기 자산은 `asset` 매개 변수로 전달되어야 합니다. JSON 기반 초기화 API를 사용하면 단일 코드 행을 사용하여 뷰어를 만들고 시작할 수 있습니다.

   뷰어 코드가 ID로 컨테이너 요소를 찾을 수 있도록 뷰어 컨테이너를 DOM에 추가해야 합니다. 일부 브라우저는 웹 페이지가 끝날 때까지 DOM 작성을 지연합니다. 그러나 호환성을 최대화하려면 닫는 `init()` 태그 바로 앞 또는 body `BODY` `onload()` 이벤트에서 메서드를 호출합니다.

   또한 컨테이너 요소가 아직 웹 페이지 레이아웃의 일부가 될 필요는 없습니다. 예를 들어, 지정된 `display:none` 스타일을 사용하여 숨길 수 있습니다. 이 경우 뷰어는 웹 페이지가 컨테이너 요소를 레이아웃으로 다시 가져올 때까지 초기화 프로세스를 지연합니다. 이 경우 뷰어 부하가 자동으로 다시 시작됩니다.

   다음은 뷰어 인스턴스를 만들고 필요한 최소 구성 옵션을 생성자에게 전달하고 `init()` 메서드를 호출하는 예입니다. 이 예제에서는 뷰어 `eCatalogSearchViewer` 인스턴스가 있다고 가정합니다.자리 표시자의 `s7viewer` 이름입니다. `DIV`;이미지 제공 `http://s7d1.scene7.com/is/image/` URL이며 `Viewers/Pluralist` 자산입니다.

   ```
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   다음 코드는 크기가 고정된 eCatalog 검색 뷰어를 포함하는 간단한 웹 페이지의 전체 예입니다.

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**제한 없는 높이로 반응형 디자인 임베드**

반응형 디자인 임베드에서는 일반적으로 웹 페이지에 뷰어의 컨테이너 런타임 크기를 지정하는 유연한 레이아웃이 `DIV`있습니다. 이 예제의 경우 웹 페이지에서 뷰어의 컨테이너에 웹 브라우저 창 크기의 40% `DIV` 를 적용할 수 있으므로 높이가 제한되지 않는다고 가정합니다. 결과 웹 페이지 HTML 코드는 다음과 같습니다.

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

이러한 페이지에 뷰어를 추가하는 것은 고정 크기 임베딩과 비슷하지만 뷰어 크기를 명시적으로 정의할 필요가 없다는 점만 다릅니다.

1. 웹 페이지에 뷰어 JavaScript 파일을 추가합니다.
1. 컨테이너 DIV를 정의합니다.
1. 뷰어를 만들고 초기화합니다.

위의 모든 단계는 고정 크기 임베딩과 동일합니다. 기존 &quot; 소유자&quot; `DIV` 에 컨테이너를 추가합니다 `DIV`. 다음 코드는 전체 예입니다. 브라우저 크기를 조정할 때 뷰어 크기가 어떻게 변경되는지, 그리고 뷰어 종횡비가 자산과 어떻게 일치하는지 볼 수 있습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

다음 예제 페이지에서는 무제한 높이로 임베드하는 응답형 디자인의 실제 사용 사례를 보여줍니다.

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**폭 및 높이가 정의된 유연한 크기 임베드**

폭 및 높이가 정의된 유연한 크기를 포함하는 경우 웹 페이지 스타일이 다릅니다. 즉, &quot;홀더&quot;에 두 가지 크기를 `DIV` 제공하고 브라우저 창에서 중앙에 배치합니다. 또한 웹 페이지는 `HTML` 및 `BODY` 요소의 크기를 100%로 설정합니다.

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

나머지 임베드 단계는 무제한 높이로 임베드하는 반응형 디자인과 동일합니다. 결과 예는 다음과 같습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter 기반 API를 사용하여 포함**

JSON 기반 초기화를 사용하는 대신 setter 기반 API와 인수 없음 생성자를 사용할 수 있습니다. 이 API 생성자는 매개 변수를 가져오지 않으며 별도의 JavaScript 호출을 사용하여 `setContainerId()`API `setParam()`및 `setAsset()` API 메서드를 사용하여 구성 매개 변수를 지정합니다.

다음 예제는 setter 기반 API를 사용한 고정 크기 임베드입니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "http://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```

