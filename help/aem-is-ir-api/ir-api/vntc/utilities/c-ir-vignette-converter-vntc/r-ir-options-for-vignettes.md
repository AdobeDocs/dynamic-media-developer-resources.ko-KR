---
description: 다음 옵션은 비네팅 파일의 처리를 제어합니다. sourceFile이 비네트가 아닌 경우 무시됩니다.
solution: Experience Manager
title: 비네팅 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# 비네팅 옵션{#options-for-vignettes}

다음 옵션은 비네팅 파일의 처리를 제어합니다. sourceFile이 비네트가 아닌 경우 무시됩니다.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -컨텐트</span> </p></td> 
  <td class="stentry"> <p>선택한 객체 속성을 포함하여 객체 계층을 나타내는 XML 파일을 생성합니다. 파일의 내용은 <span class="codeph"> req=contents</span> 명령에 의해 반환된 내용과 동일합니다. 파일의 이름은 소스 파일과 동일하지만 <span class="filepath"> .xml</span> 접미사가 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-자르기  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>크기 조절하기 전에 비네트를 자릅니다. </p> <p><span class="codeph"><span class="varname"> x</span>, <span class="varname"> </span></span> 은 자르기 사각형의 맨 위 모서리  <span class="codeph"><span class="varname"> 모서리이며 </span><span class="varname"> </span></span> 에서자르기 사각형의 크기입니다. 값은 소스 비네트의 전체 해상도 보기 이미지에 상대적인 픽셀 좌표입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidhein</span></span> </p> </td> 
  <td class="stentry"> <p>크기 조절하기 전에 비네트를 자릅니다. </p> <p><span class="codeph"><span class="varname"> xn</span>, <span class="varname"> </span></span> 자르기 사각형의 맨 위 모서리 <span class="codeph"><span class="varname"> 에 있고 </span>wdn에 <span class="varname"> </span></span> heinis가 자르기 사각형의 크기입니다. 값은 소스 비네트의 보기 이미지에 대해 표준화되며 0.0...1.0 사이여야 합니다. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinyn은 1.0보다 크지 않아야 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -임베디재</span> </p></td> 
  <td class="stentry"> <p>포함된 재료를 출력 비네트에 유지합니다. 기본적으로 출력 비네트에서 자료가 제거됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> 간격</span></span> </p></td> 
  <td class="stentry"> <p>하나 이상의 출력 비네팅 높이(픽셀 단위)입니다. -info를 지정하면 무시됩니다. <span class="varname"> </span> 는 입력 비네트의 너비를 나타내는 0일 수 있습니다. 자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> 을 참조하십시오. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>비네트에서 이미지 맵 파일을 추출할 수 있습니다. 맵 데이터는 <span class="codeph"> &lt;map&gt;</span> 요소만 포함하는 HTML 파일에 기록됩니다. 출력 파일의 이름은 출력 이미지 파일과 동일하지만 <span class="filepath"> .htm</span> 접미사가 있습니다. 명령이 지정되었지만 비네트에 맵 데이터가 없는 경우 경고 메시지가 생성되고 파일이 생성되지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -프로파일</span> </p></td> 
  <td class="stentry"> <p>비네팅에 포함된 ICC 프로파일의 복사본을 파일에 저장합니다. 명령을 지정했지만 비네트에 ICC 프로필이 없는 경우 경고 메시지가 생성되고 ICC 프로파일 파일이 생성되지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -피라미드</span> </p></td> 
  <td class="stentry"> <p>피라미드형 비네팅을 만듭니다. Dynamic Media 확대/축소 뷰어를 사용하여 렌더링된 이미지를 표시할 때 필요합니다. 자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅 크기 조정</a> 을 참조하십시오. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbnwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>축소판 이미지에 대한 픽셀 너비 및 높이 제한입니다. 지정한 경우 비네팅 보기 이미지, 캐비닛 스타일 파일의 패널 이미지 또는 Window 커버 스타일 파일의 첫 번째 스타일 조명 맵에서 <span class="varname"> ival</span> 보다 크지 않은 JPEG 이미지가 생성됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>하나 이상의 출력 비네팅 너비(픽셀 단위)입니다. <span class="codeph"> -info</span>가 지정된 경우 무시됩니다. <span class="varname"> </span> 값은 0일 수 있으며, 이것은 입력 비네트의 높이를 나타냅니다. 자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> 을 참조하십시오. </p></td> 
 </tr> 
</table>
