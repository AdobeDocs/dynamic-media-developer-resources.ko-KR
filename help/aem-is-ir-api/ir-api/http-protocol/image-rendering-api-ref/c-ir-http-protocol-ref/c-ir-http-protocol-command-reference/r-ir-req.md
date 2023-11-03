---
title: req
description: 요청 유형. 요청한 데이터 형식을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 4%

---

# req{#req}

요청 유형. 요청한 데이터 형식을 지정합니다.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 디버그 </span> </p> </td> 
  <td class="stentry"> <p>디버그 모드에서 명령을 실행합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 컨텐트 </span> </p> </td> 
  <td class="stentry"> <p>비네팅에 있는 개체에 대한 정보를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>명령을 실행하고 렌더링된 이미지를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>지정된 비네팅의 속성을 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 맵 </span> </p> </td> 
  <td class="stentry"> <p>비네팅에 포함된 이미지 맵 데이터를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 개체 </span> </p> </td> 
  <td class="stentry"> <p>명령을 실행하고 현재 개체 선택에 마스킹된 렌더링된 이미지를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>명령을 실행하고 응답 이미지의 속성을 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 사용자 데이터 </span> </p> </td> 
  <td class="stentry"> <p>다음 내용을 반환합니다. <span class="codeph"> 비네팅::UserData </span>. </p> </td> 
 </tr> 
</table>

자세한 설명에 별도로 명시되지 않는 한 서버는 MIME 유형의 텍스트 응답을 반환합니다 &lt;text plain=&quot;&quot;>.

`debug`

지정된 명령을 실행하고 렌더링된 이미지를 반환합니다. 오류가 발생하면 오류 이미지 대신 오류 및 디버그 정보가 반환됩니다( `attribute::ErrorImagePath`).

`contents`

선택한 객체 속성을 포함하여 비네팅에서 객체 계층의 XML 표현을 반환합니다. 요청의 다른 명령은 무시됩니다.

`img`

지정된 명령을 실행하고 렌더링된 이미지를 반환합니다. 응답 데이터 형식 및 응답 유형은 다음을 통해 결정됩니다. `fmt=`.

`imageprops`

URL 경로에 지정된 비네팅 파일 또는 카탈로그 항목의 선택한 속성을 반환합니다. 다음을 참조하십시오 [속성](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 응답 구문 및 응답 MIME 유형에 대한 설명입니다. 요청의 다른 명령은 무시됩니다. 다음 속성이 반환됩니다.

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>속성 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expation </span> </p> </td> 
   <td colname="col2"> <p>Double </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration </span> 또는 기본 TTL(Time to Live)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>정수 </p> </td> 
   <td colname="col3"> <p>픽셀 단위 전체 해상도 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>문자열 </p> </td> 
   <td colname="col3"> <p>이 비네팅과 연결된 프로필의 이름/설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>부울 </p> </td> 
   <td colname="col3"> <p>연결된 프로필이 비네팅에 포함된 경우 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>부울 </p> </td> 
   <td colname="col3"> <p>비네팅이 경로 데이터를 임베드하는 경우 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>문자열 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modifier </span> 카탈로그 항목이 아니면 비워 두십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>열거형 </p> </td> 
   <td colname="col3"> <p>응답 이미지의 픽셀 유형. 'CMYK', 'RGB' 또는 'BW'(회색 음영 이미지의 경우)일 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>실제 </p> </td> 
   <td colname="col3"> <p>기본 인쇄 해상도(dpi)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>문자열 </p> </td> 
   <td colname="col3"> <p>수정 날짜/시간(부터) <span class="codeph"> catalog::TimeStamp </span> 또는 비네팅 파일). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>정수 </p> </td> 
   <td colname="col3"> <p>전체 해상도 너비(픽셀 단위). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비네팅.이름 </span> </p> </td> 
   <td colname="col2"> <p>문자열 </p> </td> 
   <td colname="col3"> <p>비네팅 이름(루트 비네팅 오브젝트의 이름 문자열) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비네팅.res </span> </p> </td> 
   <td colname="col2"> <p>실제 </p> </td> 
   <td colname="col3"> <p>의 최대 오브젝트 해상도 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 물질 분해능 </a> 단위(일반적으로 픽셀/인치). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비네팅.res.avg </span> </p> </td> 
   <td colname="col2"> <p>실제 </p> </td> 
   <td colname="col3"> <p>의 평균 오브젝트 해상도 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 물질 분해능 </a> 단위(일반적으로 픽셀/포함) <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 물질 분해능 </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비네팅.res.min </span> </p> </td> 
   <td colname="col2"> <p>실제 </p> </td> 
   <td colname="col3"> <p>의 최소 오브젝트 해상도 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 물질 분해능 </a> 단위(일반적으로 픽셀/인치). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비네팅.version </span> </p> </td> 
   <td colname="col2"> <p>정수 </p> </td> 
   <td colname="col3"> <p>비네팅 파일 버전 번호입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

비네팅에 포함된 이미지 맵 데이터를 반환합니다. 기본적으로 모든 가장 바깥쪽 그룹에 대한 맵 데이터가 반환됩니다. 모든 가장 안쪽 그룹에 대한 맵 데이터는

`req=map&groupLevel=-1`

맵 데이터의 크기가 다음으로 조정되지 않음 `wid=` 또는 `hei=` 또는 그렇지 않으면 수정됩니다. 응답 MIME 유형: `<text/xml>`.

응답 데이터는 `<map>` 요소(집합 포함) `<area>` 요소, HTML과 유사 `<AREA>` 태그에 가깝게 배치하십시오.

각 `<area>` 요소에 표준 포함 `type=` 및 `coord=` 속성 및 `name=` 속성, 비네팅 그룹 이름 또는 이름 경로를 지정합니다. 복수 `<area>` 해당 개체 그룹의 마스크에 불연속 영역이 있는 경우 같은 이름의 요소가 존재합니다.

비네팅은 기본 속성 외에도 작성된 경우 추가 속성을 정의할 수 있습니다. 이러한 사용자 지정 속성을 객체 그룹 속성으로 정의합니다. 사용자 지정 특성의 이름은 다음으로 시작해야 합니다. `map` 에 포함될 내용 `<area>` 요소. 예를 들어 그룹 속성에 다음이 포함되는 경우 `map.href=http://www.scene7.com`, 해당 `<area>` 요소는 다음을 포함합니다. `href="http://www.scene7.com"`.

비어 있는 XML 문서 `<map>` 비네팅에 맵 데이터가 포함되지 않으면 요소가 반환됩니다.

`object`

지정된 명령을 실행하고 나머지 개체 선택(마지막에서 선택한 그룹 또는 개체)으로 마스킹된 렌더링된 이미지를 반환합니다. `sel=` 또는 `obj=` 명령(요청)을 참조하십시오. 일반적으로 알파를 지원하는 이미지 형식과 함께 사용됩니다(참조) [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). 알파를 지원하지 않는 이미지 형식을 사용하는 경우 마스크 외부의 영역은 검정색입니다.

`props`

지정된 명령을 실행하고 렌더링된 이미지가 아닌 비네팅 속성 및 그룹 또는 개체 속성을 반환합니다. 다음을 참조하십시오 [속성](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 응답 구문 및 응답 MIME 유형에 대한 설명입니다. 기본 선택 사항은 다음 경우에 적용됩니다. `obj=` 또는 `sel=` 도 지정됩니다(참조). [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

다음 속성이 응답에 포함될 수 있습니다.

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>속성 </p> </th> 
   <th class="entry"> <p> 유형 </p> </th> 
   <th class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>정수 </p> </td> 
   <td> <p> 응답 이미지 높이(픽셀 단위). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p>ICC 프로파일이 응답 이미지에 포함되어 있으면 참(참조) <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지와 연결된 프로필의 바로 가기 이름(참조) <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 응답 이미지에 알파가 포함되어 있으면 True입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 응답 이미지에 경로 데이터가 포함되어 있으면 참(참조) <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지 형식이며 'CMYK', 'RGB' 또는 'BW'(회색 음영 이미지의 경우)일 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> 인쇄 해상도(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>정수, 부울 </p> </td> 
   <td> <p> JPEG 품질 및 색도 플래그(참조) <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지에 대한 MIME 유형(참조) <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 응답 이미지 너비(픽셀 단위). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 현재 선택 항목에 대한 속성 문자열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 항목의 개체 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 영역의 값을 들여씁니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 선택 <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 현재 개체 선택 항목의 전체 이름 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 영역의 겹치는 오브젝트 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p>현재 선택 항목의 렌더링 가능한 개체 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 영역의 텍스트 가능 개체 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 항목의 현재 표시/숨기기 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 영역에 있는 첫 번째 오버랩 오브젝트의 Z 순서 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

다음 내용을 반환합니다. `vignette::UserData`. 서버는 다음의 모든 항목을 대체합니다. `'??'` 위치: `vignette::UserData` 라인 터미네이터 사용( `<cr><lf>`). 응답 MIME 유형이 로 설정된 텍스트 데이터로 응답 형식이 지정됩니다. &lt;text plain=&quot;&quot;>.

URL 경로에 지정된 객체가 유효한 비네팅 맵 항목으로 확인되지 않거나 `vignette::UserData` 이(가) 비어 있으면 회신에 줄 종결자( `CR/LF`).

요청 문자열의 다른 모든 명령은 무시됩니다.

## 속성 {#section-e44092e190ff4f6380583e8ed6ea5b0b}

요청 명령입니다. 요청 문자열의 어디에서나 발생할 수 있습니다.

## 기본값 {#section-00c593cbf1af4364b6b78812e6b93c64}

URL에 이미지 경로나 수정자가 포함되지 않은 경우 다음을 수행합니다.

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

그렇지 않으면, `req=img`

## 참조 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [비네팅::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [속성](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
