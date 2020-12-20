---
description: vntc는 stader 또는 로그 파일로 전송되는 텍스트 데이터를 생성합니다.
seo-description: vntc는 stader 또는 로그 파일로 전송되는 텍스트 데이터를 생성합니다.
seo-title: 출력
solution: Experience Manager
title: 출력
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# 출력{#output}

vntc는 stader 또는 로그 파일로 전송되는 텍스트 데이터를 생성합니다.

데이터는 텍스트 레코드당 하나의 `name=value` 속성 형식으로 지정됩니다. 문자열 값은 따옴표로 묶지 않습니다. `-log`이(가) 지정된 경우에도 경고 및 오류 메시지는 항상 `stderr`으로 전송됩니다.

특정 속성은 동일한 출력에서 여러 번 발생할 수 있습니다. 0으로 시작하는 시퀀스 번호가 이 속성의 이름에 마침표로 구분되어 추가됩니다. 이러한 속성은 속성 이름 뒤에 `. *`n`*` 접미어로 아래에 식별됩니다.

다음 속성이 생성됩니다.

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>캐비닛 스타일의 RGB 배경색입니다. 캐비닛 스타일만 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>기본 출력 파일 버전입니다. 또한 이 릴리스의 <span class="filepath"> vntc</span>에서 가장 높은 파일 버전 번호를 생성할 수 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">오류.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>오류 메시지. 일반적으로 오류 메시지가 있으면 출력 파일이 만들어지지 않았거나 이미지 렌더링에서 사용하는 데 적합하지 않음을 나타냅니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">파일.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>비네팅, 캐비닛 스타일 파일, 전체 해상도 이미지 및 축소판 이미지를 포함하여 모든 출력 파일의 정규화된 경로/이름입니다. 생성된 각 파일에 대해 하나의 파일 속성이 있습니다(로그 파일 제외). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 캐비닛</span> 에 유리 문이 있으면 1이고 그렇지 않으면 0입니다. 캐비닛 스타일만 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>에 포함된 iccProfile의 이름입니다. </p> <p><span class="varname"> sourceFile</span>이(가) 색상을 관리하지 않으면 비어 있습니다. 비네팅 전용. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>진행 정보 등의 정보 메시지입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> sourceFileis가  <span class="varname"> </span> 마스터 비네팅인 경우 ivalis 1이고, 이전에 vnUpdate 또는 vntc와 함께 처리된 경우  <span class="filepath"> </span> 0 <span class="filepath"> 입니다</span>. 비네팅 전용. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFileis가 </span>   <span class="varname"> </span> JPEG 이미지 데이터를 포함하는 캐비닛 스타일이면 ivalis 0(이 경우 경고도 출력됨), 그렇지 않으면 1. 스타일 파일만 덮는 캐비닛 및 창 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>실행 중인 <span class="filepath"> vntc</span> 프로세스에 적용되는 최대 메모리 제한입니다. <span class="varname"> 문자열</span> 은 ival <span class="varname"> , </span>ivalK <span class="varname"> , </span>ival <span class="varname"> m</span>  <span class="varname">  </span>  <span class="codeph">  </span> ,valG또는0(disabled)입니다. 여기서 <span class="varname"> K</span>, <span class="varname"> M</span> 및 <span class="varname"> G</span>는 KB(1024바이트), MB(1048576 바이트) 및 GB(1073741824 바이트)를 나타냅니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅에서 가장 낮은 해상도 피라미드의 크기를 지정합니다. <span class="codeph"> -pyramid</span>가 지정된 경우에만 제공됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>에 저장된 재료의 수입니다. 비네팅 전용. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>이 캐비닛 스타일 파일의 패널 이미지 수입니다. 캐비닛 스타일만 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅의 피라미드형 레벨 수입니다. -pyramid가 지정된 경우에만 표시됩니다. 비네팅 전용. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>소스 또는 대상 비네팅에 피라미드형 구조가 있는 경우 0. 비네팅 전용. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>캐비닛 스타일의 경우 <span class="varname"> sourceFile</span>의 개체 해상도입니다. 비네팅의 경우 출력 비네팅을 렌더링할 때 최상의 품질 렌더링 결과를 위해 권장되는 재료 해상도입니다. 픽셀/인치(ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅에서 가장 작은 개체 해상도입니다. 비네팅 전용. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅의 평균 개체 해상도입니다. 비네팅 전용. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>정규화된 <span class="varname"> sourceFile</span> 경로입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>의 파일 버전입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>입력 비네팅의 픽셀 크기, 캐비닛 스타일 파일의 기본 패널 이미지 또는 스타일 파일을 포함하는 윈도우의 첫 번째 불투명도 이미지입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>덮는 윈도우 유형(윈도우가 스타일을 덮는 경우에만): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=가로 음영 또는 블라인드 </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=세로 블라인드 </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=전체 폭 짧은 커튼 </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=왼쪽/오른쪽 짧은 방향 </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=전체 폭 커튼 </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=왼쪽/오른쪽 전체 길이 드래프입니다. </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=카페 커튼 </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=값 </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vntif </span> sourceFileis는  <span class="varname"> </span> 비네팅, vncif  <span class="codeph"> </span> sourceFileis <span class="varname"> </span> 는 캐비닛 스타일이나 vnwif  <span class="codeph"> </span> sourceFileis는  <span class="varname"> </span> 스타일을 포함하는 윈도우입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> -version</span>으로 지정된 값 또는<span class="codeph"> -version</span>의 값이 지정되지 않은 경우 <span class="codeph"> defaultFileVersion</span>의 값이 지정되지 않았습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span><span class="varname"> *[,</span>ival<span class="varname"> ,</span>ival]</span> </p></td> 
  <td class="stentry"> <p>출력 비네팅에 있는 모든 보기의 픽셀 크기(피라미드 비네팅의 전체 해상도 보기), 캐비닛 스타일 파일에 있는 기본 패널 이미지의 픽셀 크기 또는 스타일 파일을 포함하는 윈도우의 첫 번째 불투명도 이미지의 쉼표로 구분된 목록. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 캐비닛 </span> 스타일이 texturable이면 ivalis 1을 반환하고 그렇지 않으면 0을 반환합니다. 비네팅 및 윈도우 커버 스타일 파일에 대해서는 존재하지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">경고.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>경고 메시지(예: <span class="codeph"> -imagemap</span>이(가) 지정되었지만 비네팅에 맵 데이터가 없는 경우). </p></td> 
 </tr> 
</table>

