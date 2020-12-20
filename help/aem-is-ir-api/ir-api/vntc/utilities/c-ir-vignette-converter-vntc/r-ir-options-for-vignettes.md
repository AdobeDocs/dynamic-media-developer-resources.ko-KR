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
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# 비네팅 옵션{#options-for-vignettes}

다음 옵션은 비네팅 파일의 처리를 제어합니다. sourceFile이 비네팅이 아닌 경우 무시됩니다.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -컨텐트</span> </p></td> 
  <td class="stentry"> <p>객체 계층 구조를 나타내는 XML 파일을 만들고 선택한 객체 속성을 포함합니다. 파일의 내용은 <span class="codeph"> req=contents</span> 명령에 의해 반환된 내용과 동일합니다. 파일의 이름은 소스 파일과 동일하지만 <span class="filepath"> .xml</span> 접미어를 사용합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>크기를 조절하기 전에 비네팅을 자릅니다. </p> <p><span class="codeph"><span class="varname"> x</span><span class="varname"> </span></span> 는 자르기 사각형의 맨 위 <span class="codeph"><span class="varname"> 의</span> 모서리<span class="varname"> </span></span> 로 자르기 사각형의 크기를 나타냅니다. 값은 소스 비네팅의 전체 해상도 보기 이미지를 기준으로 하는 픽셀 좌표입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidenhein</span></span> </p> </td> 
  <td class="stentry"> <p>크기를 조절하기 전에 비네팅을 자릅니다. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> </span></span> yn <span class="codeph"><span class="varname">  자르기 사각형의 맨 위 모서리</span>에 있는<span class="varname"> </span></span>  경우, heinhein은 자르기 사각형의 크기입니다. 값은 소스 비네팅의 보기 이미지를 기준으로 표준화되며 0.0...1.0 사이여야 합니다. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinhein은 1.0보다 크지 않아야 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -임베드 자료</span> </p></td> 
  <td class="stentry"> <p>포함된 재질을 출력 비네팅에 유지합니다. 기본적으로 자재는 출력 비네팅에서 제거됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>하나 이상의 출력 비네팅 높이(픽셀 단위)입니다. -info가 지정된 경우 무시됩니다. <span class="varname"> 입력 비네팅의 폭을 나타내는 값</span> 은 0일 수 있습니다. 자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅 크기 조절</a>을 참조하십시오. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>비네팅에서 이미지 맵 파일을 추출할 수 있습니다. 맵 데이터는 <span class="codeph"> &lt;map&gt;</span> 요소만 포함하는 HTML 파일에 기록됩니다. 출력 파일의 이름은 출력 이미지 파일과 동일하지만 <span class="filepath"> .htm</span> 접미어를 사용합니다. 명령을 지정했지만 비네팅에 맵 데이터가 없는 경우 경고 메시지가 생성되고 파일이 생성되지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -프로파일</span> </p></td> 
  <td class="stentry"> <p>비네팅에 포함된 ICC 프로필의 복사본을 파일에 저장합니다. 명령을 지정했지만 비네팅에 ICC 프로파일이 없는 경우 경고 메시지가 생성되고 ICC 프로파일 파일이 생성되지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -피라미드</span> </p></td> 
  <td class="stentry"> <p>피라미드형 비네팅을 만듭니다. Scene7 확대/축소 뷰어를 사용하여 렌더링된 이미지를 표시하는 데 필요합니다. 자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅 크기 조절</a>을 참조하십시오. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>축소판 이미지에 대한 픽셀 너비 및 높이 제한. 지정된 경우 비네팅 보기 이미지, 캐비닛 스타일 파일의 패널 이미지 또는 윈도우 커버 스타일 파일의 첫 번째 스타일 조명 맵에서 <span class="varname"> 간격</span>보다 크지 않은 JPEG 이미지가 생성됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> val</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>하나 이상의 출력 비네팅 폭(픽셀 단위)입니다. <span class="codeph"> -info</span>가 지정된 경우 무시됩니다. <span class="varname"> 입력 </span> 비네팅의 높이를 나타내는 0일 수 있습니다. 자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅 크기 조절</a>을 참조하십시오. </p></td> 
 </tr> 
</table>

