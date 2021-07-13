---
description: vntc는 stderr 또는 로그 파일로 전송되는 텍스트 데이터를 생성합니다.
solution: Experience Manager
title: 출력
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 출력{#output}

vntc는 stderr 또는 로그 파일로 전송되는 텍스트 데이터를 생성합니다.

데이터는 텍스트 레코드당 하나의 `name=value` 속성으로 지정됩니다. 문자열 값은 따옴표로 묶이지 않습니다. `-log` 이 지정되어 있어도 경고 및 오류 메시지는 항상 `stderr`으로 전송됩니다.

특정 속성은 동일한 출력에 여러 번 발생할 수 있습니다. 0으로 시작하는 시퀀스 번호가 이러한 속성의 이름에 마침표로 구분되어 추가됩니다. 이러한 속성은 속성 이름 뒤에 `. *`n`*` 접미사를 사용하여 아래에 식별됩니다.

다음 속성이 생성됩니다.

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>, <span class="varname"> ival</span>, <span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>캐비닛 스타일의 RGB 배경색입니다. 캐비닛 스타일만 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>기본 출력 파일 버전입니다. 또한 이 릴리스의 가장 높은 파일 버전 번호 <span class="filepath"> vntc</span>가 생성할 수 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">오류.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>오류 메시지. 오류 메시지가 표시된다면 일반적으로 출력 파일이 만들어지지 않거나 이미지 렌더링에서 사용하는 데 적합하지 않은 것입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">파일.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>비네팅, 캐비닛 스타일 파일, 전체 해상도 이미지 및 축소판 이미지를 포함하여 모든 출력 파일의 정규화된 경로/이름입니다. 생성된 각 파일(로그 파일 제외)에 하나의 파일 속성이 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> 캐비닛에 유리문이 있으면 1이고, 없으면 0입니다. 캐비닛 스타일만 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>에 포함된 iccProfile의 이름입니다. </p> <p><span class="varname"> sourceFile</span>이 색상 관리가 아닌 경우 비어 있습니다. 비네팅만 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>진행 정보 등의 정보 메시지입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> sourceFile이 마스터  <span class="varname"> </span> 비네팅인 경우 ivalis 1, vnUpdateor vntc <span class="filepath"> </span> 로 이전에 처리된 경우  <span class="filepath"> 0</span>입니다. 비네팅만 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> sourceFileis가 JPEG 이미지 데이터 <span class="varname"> </span> 가 포함된 캐비닛 스타일인 경우 ivalis 0이고, 그렇지 않으면 1입니다. 스타일 파일만 덮는 캐비닛 및 창 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>실행 중인 <span class="filepath"> vntc</span> 프로세스에 적용되는 최대 메모리 제한입니다. <span class="varname"> </span> 문자열은  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> 또는  <span class="codeph"> 0</span> (비활성화)입니다. 여기서 <span class="varname"> K</span>, <span class="varname"> M</span> 및 <span class="varname"> G</span>는 킬로바이트(1024바이트), 메가바이트(1048576 바이트) 및 기가바이트(1073741824바이트)를 참조합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네트에서 가장 낮은 해상도 피라미드 수준의 배율. <span class="codeph"> -pyramid</span>가 지정된 경우에만 표시됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>에 저장된 자료 수입니다. 비네팅만 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> val</span></span> </p></td> 
  <td class="stentry"> <p>이 캐비닛 스타일 파일의 패널 이미지 수입니다. 캐비닛 스타일만 합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네트의 피라미드 레벨 수입니다. -pyramid가 지정된 경우에만 표시됩니다. 비네팅만 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>소스 또는 대상 비네트에 피라미드형 구조가 있는 경우 0입니다. 비네팅만 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>캐비닛 스타일의 경우 <span class="varname"> sourceFile</span>의 개체 해상도입니다. 비네팅의 경우 출력 비네팅을 렌더링할 때 최상의 품질 렌더링 결과를 위해 권장되는 재료 해상도입니다. 픽셀/인치(ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅에서 가장 작은 개체 해상도입니다. 비네팅만 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네트의 평균 개체 해상도. 비네팅만 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>정규화된 <span class="varname"> sourceFile</span> 경로입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span> 파일 버전입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> val</span>, <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>입력 비네트의 픽셀 크기, 캐비닛 스타일 파일의 기본 패널 이미지 또는 스타일 파일을 덮는 창의 첫 번째 불투명도 이미지. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>창 덮개의 유형(윈도우 덮개에만 해당): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=가로 음영 또는 블라인드 </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=세로 블라인드 </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=폭 짧은 커튼 </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=왼쪽/오른쪽 짧은 공백 </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=풀폭 풀길이 커튼 </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=왼쪽/오른쪽 전체 길이 커튼 </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=카페 커튼 </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=값 </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFileis는 비네트이고  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFileis는 캐비닛 스타일입니다. 또는  <span class="codeph"> </span> vnwif sourceFileis는  <span class="varname"> </span> 스타일을 포함하는 창입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> -version</span> 또는 <span class="codeph"> defaultFileVersion</span> 값이 지정되지 않은 경우 <span class="codeph"> -version</span> 값을 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSize=<span class="varname"> val</span>, <span class="varname"> val</span>*[,<span class="varname"> val</span>, <span class="varname"> val</span>]</span> </p></td> 
  <td class="stentry"> <p>출력 비네팅(피라미드 비네팅을 위한 전체 해상도 보기)의 모든 뷰의 픽셀 크기 목록, 캐비닛 스타일 파일의 기본 패널 이미지 또는 스타일 파일을 덮는 창의 첫 번째 불투명도 이미지의 쉼표로 구분된 목록입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> 캐비닛 스타일이 텍스쳐일 수 있으면 1이고 그렇지 않으면 0입니다. 비네팅 및 창 커버링 스타일 파일에 사용할 수 없습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">경고.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>경고 메시지(예: <span class="codeph"> -imagemap</span>이 지정되었지만 비네트에 맵 데이터가 없는 경우). </p></td> 
 </tr> 
</table>
