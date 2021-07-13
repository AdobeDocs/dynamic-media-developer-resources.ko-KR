---
description: Image Serving은 text= 및 textPs= 명령으로 액세스할 수 있는 텍스트 렌더링에 대한 여러 가지 대체 요소를 제공합니다.
solution: Experience Manager
title: 텍스트 서식
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 7%

---

# 텍스트 서식{#text-formatting}

Image Serving은 text= 및 textPs= 명령으로 액세스할 수 있는 텍스트 렌더링에 대한 여러 가지 대체 요소를 제공합니다.

`textPs=` Adobe Photoshop 및 Illustrator으로 렌더링된 텍스트와 높은 수준의 유사성을 제공합니다. `text=` 는 Windows Wordpad에서 렌더링되는 텍스트와 상당히 호환됩니다.

>[!NOTE]
>
>다른 곳에 나열된 차이 외에도 `text=`은 `textPs=`과 비교할 때 렌더링된 텍스트에서 미묘한 차이를 만듭니다. 예를 들어, 밑줄은 두께와 위치가 동일하지 않고 합성 기울임체가 약간 다른 각도로 렌더링됩니다. 텍스트가 사용 가능한 공간에 맞지 않는 경우 `text=`은 마지막 줄을 부분적으로 자르는 반면, `textPs=`은 전체 줄만 렌더링합니다.

모든 텍스트 명령은 RTF(리치 텍스트 형식) 사양과 함께 서식 있는 텍스트를 허용합니다. 각 텍스트 레이어마다 다른 텍스트 명령을 지정할 수 있습니다.

다음 표에는 각 텍스트 명령에 사용할 수 있는 주요 기능이 나와 있습니다.

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 기능</b> </th> 
   <th class="entry"> <b> 텍스트=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> 참조</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop 호환 가능 </p> </td> 
   <td> <p> 아니오 </p> </td> 
   <td> <p> 제한된 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>임의의 도형으로 텍스트 흐름 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>임의의 경로를 따라 텍스트 흐름 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>복사 피팅 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> 복사 피팅 <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>텍스트 상자 여백 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>전체 단락 양쪽 맞춤 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>마지막 줄 맞춤 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>단락 들여쓰기 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>모든 대문자 및 작은 대문자 텍스트 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>이미지 제공 색상 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>여러 앤티앨리어싱 모드 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>위쪽/오른쪽 텍스트 흐름 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>\sttextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Photoshop® 지원 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> 글꼴 처리 </td> 
  </tr> 
  <tr> 
   <td> <p>텍스트에 맞게 레이어 자동 크기 조정 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK 지원 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>오른쪽에서 왼쪽 쓰기 문자 흐름 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>자동 줄 바꿈 사용 안 함 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>해상도를 달리하여 레이어에 맞게 텍스트 자동 크기 조정 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF 호환 문자열은 수동으로 또는 RTF 파일을 저장할 수 있는 텍스트 편집기나 워드 프로세서에 원하는 텍스트를 포맷하여 어셈블할 수 있습니다. 그러면 RTF 파일을 일반 텍스트 편집기에서 열 수 있으며, 요청 URL에 복사된 파일의 관련 원시 RTF 컨텐트를 열 수 있습니다.

일부 워드 프로세서는 큰 파일을 생성하며, 여기에는 Dynamic Media 이미지 제공 시 사용되지 않는 상당한 프리앰블이 포함됩니다. 문자열을 텍스트 명령에 전달하기 전에 문자열에서 사용하지 않은 RTF 요소를 제거하는 것이 좋습니다.

UTF-8 및 ISO 표준을 기반으로 하는 언어 인코딩은 표준 RTF 문자 인코딩 메커니즘의 대체 요소로 RTF 문자열에서 지원됩니다. 이렇게 하면 응용 프로그램에서 RTF 인코딩에 대한 지식이 없는 상태로 서버에 영어 이외의 텍스트를 보낼 수 있습니다.

http를 통해 문자열을 전송해야 하는 경우 HTTP 규격 이외의 모든 문자를 올바르게 이스케이프해야 합니다. 문자열을 이미지 카탈로그 레코드의 `catalog::Modifiers` 필드에 통합하는 경우 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;만 이스케이프해야 합니다. `<CR>`, `<LF>` 및 `<TAB>`를 포함하는 제어 문자는 항상 제거해야 합니다.

이미지 제공 텍스트 엔진은 서식 있는 텍스트 형식(RTF) 사양, 버전 1.6으로 정의된 하위 명령 집합을 해석합니다. 이 하위 집합은 글꼴/문자 서식, 간단한 단락 서식, 국제 글꼴 및 문자 집합에 대한 지원에 중점을 둡니다. 스타일시트 및 테이블과 같은 고급 서식 구문은 현재 지원되지 않습니다.

Microsoft에서 게시한 리치 텍스트 형식(RTF) 사양에 대해 잘 알고 있어야 RTF로 인코딩된 텍스트 문자열을 수동으로 구성할 수 있습니다.

* [글꼴 처리](r-font-handling.md)
* [색상 처리](r-color-handling.md)
* [복사 피팅](r-copy-fitting.md)
* [텍스트 레이어](r-text-layers.md)
* [텍스트 위치 지정](r-text-positioning.md)
* [예약된 문자](r-reserved-characters.md)
* [지원되는 RTF 명령 및 키워드](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF 인코딩 예](r-rtf-encoding-examples.md)
