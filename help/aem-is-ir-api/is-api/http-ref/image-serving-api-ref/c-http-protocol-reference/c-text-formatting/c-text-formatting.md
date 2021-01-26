---
description: 이미지 제공에서는 text= 및 textPs= 명령을 사용하여 액세스할 수 있는 텍스트 렌더링에 대한 여러 가지 대체 요소를 제공합니다.
seo-description: 이미지 제공에서는 text= 및 textPs= 명령을 사용하여 액세스할 수 있는 텍스트 렌더링에 대한 여러 가지 대체 요소를 제공합니다.
seo-title: 텍스트 서식
solution: Experience Manager
title: 텍스트 서식
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 6%

---


# 텍스트 서식 지정{#text-formatting}

이미지 제공에서는 text= 및 textPs= 명령을 사용하여 액세스할 수 있는 텍스트 렌더링에 대한 여러 가지 대체 요소를 제공합니다.

`textPs=` adobe photoshop 및 Illustrator으로 렌더링된 텍스트와 유사성이 높은 수준을 제공합니다. `text=` 은 Windows Wordpad에서 렌더링된 텍스트와 상당히 호환됩니다.

>[!NOTE]
>
>다른 곳에 나열된 차이점 외에도 `text=`은 `textPs=`과 비교할 때 렌더링된 텍스트에서 미묘한 차이를 만듭니다. 예를 들어 밑줄은 두께와 위치가 동일하지 않으며 합성된 기울임체가 약간 다른 각도로 렌더링됩니다. 텍스트가 사용 가능한 공간에 맞지 않는 경우 `text=`은 마지막 행을 부분적으로 자를 수 있으며, `textPs=`은 전체 줄만 렌더링합니다.

모든 텍스트 명령은 RTF(Rich Text Format) 사양의 하위 집합을 기준으로 서식이 지정된 텍스트를 허용합니다. 각 텍스트 레이어는 다른 텍스트 명령을 지정할 수 있습니다.

다음 표에는 각 텍스트 명령에 사용할 수 있는 주요 기능이 나열되어 있습니다.

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
   <td> <p> Adobe Photoshop 호환 </p> </td> 
   <td> <p> 아니오 </p> </td> 
   <td> <p> 제한된 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>임의의 모양으로 텍스트 흐름 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>임의의 패스를 따라 텍스트 흐름 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>복사 맞춤 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> 복사 맞춤 <p>, <pre>\자동 맞춤</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>텍스트 상자 여백 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margart</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>전체 단락 맞춤 설정 </p> </td> 
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
   <td> <p>여러 앤티 앨리어스 모드 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>위쪽/오른쪽 텍스트 흐름 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>\stextFlow </p> </td> 
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
   <td> <p>오른쪽에서 왼쪽으로 쓰는 문자 흐름 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>줄 바꿈 비활성화 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>다양한 해상도로 레이어에 맞게 텍스트 크기 자동 조정 </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF 호환 문자열은 수동으로 어셈블하거나 RTF 파일을 저장할 수 있는 텍스트 편집기 또는 워드 프로세서에서 원하는 텍스트의 서식을 지정하여 어셈블할 수 있습니다. 그런 다음 RTF 파일을 일반 텍스트 편집기에서 열 수 있으며, 요청 URL에 복사한 파일의 관련 원시 RTF 콘텐트입니다.

일부 워드 프로세서는 Dynamic Media 이미지 서비스 기능에서 사용하지 않는 수준 높은 전문을 포함하는 대용량 파일을 생성합니다. 텍스트 명령에 문자열을 전달하기 전에 문자열에서 사용하지 않는 RTF 요소를 제거하는 것이 좋습니다.

UTF-8 및 ISO 표준을 기반으로 하는 언어 인코딩은 표준 RTF 문자 인코딩 메커니즘의 대안으로 RTF 문자열에서 지원됩니다. 따라서 응용 프로그램에서 RTF 인코딩에 대한 지식 없이 영어 이외의 텍스트를 서버로 보낼 수 있습니다.

http를 통해 문자열을 전송하려면 HTTP를 준수하지 않는 모든 문자를 제대로 escape해야 합니다. 문자열이 이미지 카탈로그 레코드의 `catalog::Modifiers` 필드에 포함된 경우 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;만 이스케이프해야 합니다. `<CR>`, `<LF>` 및 `<TAB>`를 비롯한 제어 문자는 항상 제거해야 합니다.

Image Serving 텍스트 엔진은 RTF(Rich Text Format) 사양, 버전 1.6에서 정의한 하위 명령 세트를 해석합니다. 이 하위 세트는 글꼴/문자 서식 지정, 간단한 단락 서식 지정 및 국제 글꼴 및 문자 집합에 대한 지원에 중점을 둡니다. 스타일 시트 및 표와 같은 고급 서식 지정 구문은 현재 지원되지 않습니다.

Microsoft에서 게시한 RTF(Rich Text Format) 사양에 익숙하기 때문에 RTF 인코딩 텍스트 문자열을 수동으로 만들려는 경우 필요합니다.

* [글꼴 처리](r-font-handling.md)
* [색상 처리](r-color-handling.md)
* [복사 맞춤](r-copy-fitting.md)
* [텍스트 레이어](r-text-layers.md)
* [텍스트 배치](r-text-positioning.md)
* [예약된 문자](r-reserved-characters.md)
* [지원되는 RTF 명령 및 키워드](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF 인코딩 예제](r-rtf-encoding-examples.md)
