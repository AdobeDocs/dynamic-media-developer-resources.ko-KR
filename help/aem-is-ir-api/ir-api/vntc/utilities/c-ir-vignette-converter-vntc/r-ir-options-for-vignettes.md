---
description: 다음 옵션은 비네팅 파일의 처리를 제어합니다. sourceFile이 비네팅이 아닌 경우 무시됩니다.
solution: Experience Manager
title: 비네팅 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 비네팅 옵션{#options-for-vignettes}

다음 옵션은 비네팅 파일의 처리를 제어합니다. sourceFile이 비네팅이 아닌 경우 무시됩니다.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -컨텐트</span> </p></td> 
  <td class="stentry"> <p>개체 계층 구조를 나타내고 선택한 개체 특성을 포함하는 XML 파일을 만듭니다. 파일의 내용은 가 반환하는 것과 같습니다 <span class="codeph"> req=contents</span> 명령입니다. 파일의 이름은 소스 파일과 같지만 <span class="filepath"> .xml</span> 접미사. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>크기 조정하기 전에 비네팅을 자릅니다. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> 자르기 사각형의 위쪽 왼쪽 모서리입니다. <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> 은 자르기 사각형의 크기입니다. 값은 소스 비네팅의 전체 해상도 보기 이미지에 상대적인 픽셀 좌표입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> 와이든</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>크기 조정하기 전에 비네팅을 자릅니다. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> 자르기 사각형의 위쪽 왼쪽 모서리입니다. <span class="codeph"><span class="varname"> 와이든</span>,<span class="varname"> hein</span></span> 은 자르기 사각형의 크기입니다. 값은 소스 비네팅의 보기 이미지를 기준으로 표준화되며 0.0...1.0 사이여야 합니다. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> 와이든</span></span> 및 <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> 은(는) 1.0보다 크지 않아야 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 임베디드 재료</span> </p></td> 
  <td class="stentry"> <p>포함된 재료를 출력 비네팅에 유지합니다. 기본적으로 재료는 출력 비네팅에서 제거됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>하나 이상의 출력 비네팅 높이(픽셀 단위)입니다. -info가 지정된 경우 무시됩니다. <span class="varname"> 이발</span> 입력 비네팅의 폭을 나타내는 0일 수 있다. 다음을 참조하십시오 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅 크기 조절</a> 을 참조하십시오. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>비네팅에서 이미지 맵 파일의 추출을 활성화합니다. HTML 맵 데이터는 <span class="codeph"> &lt;map&gt;</span> 요소를 생성하지 않습니다. 출력 파일의 이름은 출력 이미지 파일과 동일하지만 <span class="filepath"> .htm</span> 접미사. 명령이 지정되었지만 비네팅에 맵 데이터가 없는 경우 경고 메시지가 생성되고 파일이 생성되지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -프로파일</span> </p></td> 
  <td class="stentry"> <p>비네팅에 포함된 ICC 프로파일의 복사본을 파일에 저장합니다. 명령을 지정했지만 비네팅에 ICC 프로파일이 없는 경우 경고 메시지가 생성되고 ICC 프로파일 파일이 생성되지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -피라미드형</span> </p></td> 
  <td class="stentry"> <p>피라미드형 비네팅을 만듭니다. 렌더링된 이미지가 Dynamic Media 확대/축소 뷰어와 함께 표시될 때 필요합니다. 다음을 참조하십시오 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅 크기 조절</a> 추가 정보. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>썸네일 이미지에 대한 픽셀 너비 및 높이 제한입니다. 지정하면 더 넓지 않고 더 크지 않은 JPEG 이미지가 표시됩니다. <span class="varname"> 이발</span> 는 비네팅 보기 이미지, 캐비닛 스타일 파일의 패널 이미지 또는 창 전환 스타일 파일의 첫 번째 스타일의 조명 맵에서 생성됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> 이발</span> *[,<span class="varname"> 이발</span>]</span> </p></td> 
  <td class="stentry"> <p>하나 이상의 출력 비네팅 너비(픽셀 단위). 다음과 같은 경우 무시됨 <span class="codeph"> -info</span> 이(가) 지정되었습니다. <span class="varname"> 이발</span> 입력 비네팅의 높이를 나타내는 0일 수 있다. 다음을 참조하십시오 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 비네팅 크기 조절</a> 을 참조하십시오. </p></td> 
 </tr> 
</table>
