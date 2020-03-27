---
description: 다음 옵션은 비네팅 파일의 처리를 제어합니다. sourceFile이 비네팅이 아닌 경우 무시됩니다.
seo-description: 다음 옵션은 비네팅 파일의 처리를 제어합니다. sourceFile이 비네팅이 아닌 경우 무시됩니다.
seo-title: 비네팅 옵션
solution: Experience Manager
title: 비네팅 옵션
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 비네팅 옵션{#options-for-vignettes}

다음 옵션은 비네팅 파일의 처리를 제어합니다. sourceFile이 비네팅이 아닌 경우 무시됩니다.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -컨텐트</span> </p></td> 
  <td class="stentry"> <p>선택한 객체 속성을 포함하여 객체 계층을 나타내는 XML 파일을 만듭니다. 파일의 내용은 req=contents <span class="codeph"> 명령에서</span> 반환된 내용과 동일합니다. 파일의 이름은 소스 파일과 동일하지만 <span class="filepath"> .xml</span> 접미어를 붙입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>크기를 조절하기 전에 비네팅을 자릅니다. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> 는 <span class="codeph"><span class="varname"> 사각형 자르기 사각형의 맨 위</span>모서리이고,<span class="varname"> wid는</span></span> 사각형 자르기 크기입니다. 값은 소스 비네팅의 전체 해상도 보기 이미지를 기준으로 하는 픽셀 좌표입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> wnd</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>크기를 조절하기 전에 비네팅을 자릅니다. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> 은 <span class="codeph"><span class="varname"> 자르기 사각형의 맨 위 모서리,</span>그<span class="varname"> 이유는</span></span> 자르기 사각형의 크기입니다. 값은 소스 비네팅의 보기 이미지를 기준으로 표준화되며 0.0...1.0 사이여야 합니다. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> wid</span></span> 및 <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein은</span></span> 1.0보다 크지 않아야 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -임베드 자료</span> </p></td> 
  <td class="stentry"> <p>포함된 자료를 출력 비네팅에 그대로 유지할 수 있습니다. 기본적으로 자재는 출력 비네팅에서 제거됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>하나 이상의 출력 비네팅 높이(픽셀 단위) -info가 지정된 경우 무시됩니다. <span class="varname"> ival</span> 은 입력 비네팅의 너비를 나타내는 0일 수 있습니다. 자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅</a> 크기 조정을 참조하십시오. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>비네팅에서 이미지 맵 파일을 추출할 수 있습니다. 맵 데이터는 <span class="codeph"> &lt;map&gt;</span> 요소만 포함하는 HTML 파일에 기록됩니다. 출력 파일의 이름은 출력 이미지 파일과 같지만 <span class="filepath"> .htm</span> 접미사를 붙입니다. 명령을 지정했지만 맵 데이터가 비네팅에 없는 경우 경고 메시지가 생성되고 파일이 생성되지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -프로파일</span> </p></td> 
  <td class="stentry"> <p>비네팅에 포함된 ICC 프로필의 사본을 파일에 저장합니다. 명령을 지정했지만 비네팅에 ICC 프로필이 없는 경우 경고 메시지가 생성되고 ICC 프로필 파일이 생성되지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -피라미드</span> </p></td> 
  <td class="stentry"> <p>피라미드 비네팅을 만듭니다. 렌더링된 이미지가 Scene7 확대/축소 뷰어와 함께 표시되어야 하는 경우 필요합니다. 자세한 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 내용은 비네팅</a> 크기 조정을 참조하십시오. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>축소판 이미지의 픽셀 너비 및 높이 제한. 이 옵션을 지정하면 비네팅 보기 이미지, 캐비닛 스타일 파일의 패널 이미지 또는 윈도우 커버 스타일 파일의 첫 번째 스타일 조명 맵에서 <span class="varname"></span> 더 넓거나 크기 이하의 JPEG 이미지가 생성됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>하나 이상의 출력 비네팅 폭(픽셀 단위)이 -info <span class="codeph"> 가</span> 지정된 경우 무시됩니다. <span class="varname"> ival</span> 은 입력 비네팅의 높이를 나타내는 0일 수 있습니다. 자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅</a> 크기 조정을 참조하십시오. </p></td> 
 </tr> 
</table>

