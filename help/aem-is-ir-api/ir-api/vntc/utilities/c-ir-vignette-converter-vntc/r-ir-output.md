---
description: vntc는 stderr 또는 로그 파일로 전송되는 텍스트 데이터를 생성합니다.
solution: Experience Manager
title: 출력
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# 출력{#output}

vntc는 stderr 또는 로그 파일로 전송되는 텍스트 데이터를 생성합니다.

데이터 형식이 하나로 지정됩니다. `name=value` 텍스트 레코드당 속성입니다. 문자열 값은 따옴표로 묶이지 않습니다. 경고 및 오류 메시지는 항상 (으)로 전송됩니다. `stderr`, 비록 `-log` 이(가) 지정되었습니다.

특정 속성은 동일한 출력에서 여러 번 발생할 수 있습니다. 0으로 시작하는 시퀀스 번호는 이러한 속성의 이름에 마침표로 구분되어 추가됩니다. 이러한 속성은 다음과 같이 식별됩니다. `. *`n`*` 속성 이름 뒤에 접미사가 붙습니다.

다음 속성이 생성됩니다.

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> 이발</span>,<span class="varname"> 이발</span>,<span class="varname"> 이발</span></span> </p> </td> 
  <td class="stentry"> <p>캐비닛 스타일의 RGB 배경색입니다. 캐비닛 스타일만. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>기본 출력 파일 버전입니다. 또한 이번 릴리스에서 가장 높은 파일 버전 번호 <span class="filepath"> vntc</span> 생성할 수 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">오류.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>오류 메시지. 오류 메시지가 있으면 일반적으로 출력 파일이 만들어지지 않았거나 이미지 렌더링에 적합하지 않음을 나타냅니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">파일.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>비네팅, 캐비닛 스타일 파일, 전체 해상도 이미지 및 축소판 이미지를 포함한 모든 출력 파일의 정규화된 경로/이름입니다. 생성된 각 파일(로그 파일 제외)에 대해 하나의 파일 속성이 존재합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">유리=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 이발</span> 캐비닛에 유리 도어가 포함되어 있으면 1, 그렇지 않으면 0입니다. 캐비닛 스타일만. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>에 포함된 iccProfile의 이름 <span class="varname"> sourceFile</span>. </p> <p>다음과 같은 경우 비어 있음 <span class="varname"> sourceFile</span> 은(는) 색상 관리되지 않습니다. 비네팅만 해당. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>정보 메시지(예: 진행 정보) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 이발</span> 이면 1임 <span class="varname"> sourceFile</span> 은(는) 이전에 로 처리된 경우 0인 마스터 비네팅입니다. <span class="filepath"> vnUpdate</span> 또는 <span class="filepath"> vntc</span>. 비네팅만 해당. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 이발</span> 이면 0임 <span class="varname"> sourceFile</span> 는 JPEG 이미지 데이터를 포함하는 캐비닛 스타일이며(이 경우 경고도 출력됨), 그렇지 않으면 1입니다. 캐비닛 및 창 커버링 스타일 파일만. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>실행 중인 항목에 적용되는 최대 메모리 제한 <span class="filepath"> vntc</span> 프로세스. <span class="varname"> 문자열</span> 다음 중 하나 <span class="varname"> 이발</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span>, 또는 <span class="codeph"> 0</span> (비활성화됨). 위치 <span class="varname"> K</span>, <span class="varname"> M</span>, 및 <span class="varname"> G</span> 킬로바이트(1024바이트), 메가바이트(1048576바이트) 및 기가바이트(1073741824바이트)를 참조하십시오. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅에서 가장 낮은 해상도 피라미드 수준의 비율입니다. 다음과 같은 경우에만 있음 <span class="codeph"> -피라미드형</span> 이(가) 지정되었습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>에 저장된 재료 수 <span class="varname"> sourceFile</span>. 비네팅만 해당. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>이 캐비닛 스타일 파일의 패널 이미지 수입니다. 캐비닛 스타일만. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅의 피라미드 수준 수입니다. -pyramid가 지정된 경우에만 표시됩니다. 비네팅만 해당. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">피라미드형=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>소스 또는 대상 비네팅 중 하나에 피라미드 구조가 있는 경우 0. 비네팅만 해당. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">해상도=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>캐비닛 스타일의 경우 개체 해상도<span class="varname"> sourceFile</span>. 비네팅의 경우 출력 비네팅을 렌더링할 때 최상의 품질 렌더링 결과를 위한 권장 재료 해상도입니다. 픽셀/인치(ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅에서 가장 작은 개체 해상도입니다. 비네팅만 해당. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>출력 비네팅의 평균 개체 해상도입니다. 비네팅만 해당. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>완전한 자격을 갖춘 <span class="varname"> sourceFile</span> 경로. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>의 파일 버전 <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> 이발</span>,<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>입력 비네팅의 픽셀 크기, 캐비닛 스타일 파일의 기본 패널 이미지 또는 창 커버링 스타일 파일의 첫 번째 불투명도 이미지. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>창 커버링 유형(창 커버링 스타일만 해당): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=가로 음영 또는 블라인드 </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=수직 블라인드 </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=전폭 짧은 커튼 </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=왼쪽/오른쪽 짧은 드레이프 </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=전폭 커튼 </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=왼쪽/오른쪽 전체 길이 드레이프 </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=카페 커튼 </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> if <span class="varname"> sourceFile</span> 비네팅이고, <span class="codeph"> vnc</span> if <span class="varname"> sourceFile</span> 캐비닛 스타일이거나 <span class="codeph"> vnw</span> if <span class="varname"> sourceFile</span> 창 커버링 스타일입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p>지정된 값 <span class="codeph"> -version</span>또는 값<span class="codeph"> 기본 파일 버전</span> if<span class="codeph"> -version</span> 이(가) 지정되지 않았습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> 이발</span>,<span class="varname"> 이발</span>*[,<span class="varname"> 이발</span>,<span class="varname"> 이발</span>]</span> </p></td> 
  <td class="stentry"> <p>출력 비네팅(피라미드형 비네팅의 전체 해상도 보기)에 있는 모든 보기, 캐비닛 스타일 파일에 있는 기본 패널 이미지 또는 창 커버링 스타일 파일의 첫 번째 불투명도 이미지의 픽셀 크기를 쉼표로 구분한 목록입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">텍스트 가능=<span class="varname"> 이발</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 이발</span> 캐비닛 스타일이 텍스처화할 수 있으면 1이고, 그렇지 않으면 0입니다. 비네팅 및 창 표지 스타일 파일은 없습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">경고.<span class="varname"> n</span>=<span class="varname"> 문자열</span></span> </p></td> 
  <td class="stentry"> <p>경고 메시지(예: <span class="codeph"> -imagemap</span> 가 지정되었지만 비네팅에서 맵 데이터를 찾을 수 없습니다. </p></td> 
 </tr> 
</table>
