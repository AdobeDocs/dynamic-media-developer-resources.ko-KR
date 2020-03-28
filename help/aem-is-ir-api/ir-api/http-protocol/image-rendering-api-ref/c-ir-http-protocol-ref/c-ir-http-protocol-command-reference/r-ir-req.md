---
description: 요청 유형. 요청한 데이터 유형을 지정합니다.
seo-description: 요청 유형. 요청한 데이터 유형을 지정합니다.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dd13338-3457-477f-96e7-3ace7266d0ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# req{#req}

요청 유형. 요청한 데이터 유형을 지정합니다.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 디버그 </span> </p> </td> 
  <td class="stentry"> <p>디버그 모드에서 명령을 실행합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 컨텐트 </span> </p> </td> 
  <td class="stentry"> <p>비네팅의 개체에 대한 정보를 반환합니다. </p> </td> 
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
  <td class="stentry"> <p>명령을 실행하고 현재 개체 선택 영역에 마스크된 렌더링된 이미지를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>명령을 실행하고 응답 이미지의 속성을 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 사용자 데이터 </span> </p> </td> 
  <td class="stentry"> <p>vignette:: <span class="codeph"> UserData의 내용을 반환합니다 </span>. </p> </td> 
 </tr> 
</table>

자세한 설명에 별도로 명시되지 않는 한, 서버는 MIME 유형이 &lt;text/plain>인 텍스트 응답을 반환합니다.

`debug`

지정된 명령을 실행하고 렌더링된 이미지를 반환합니다. 오류가 발생하면 오류 이미지( `attribute::ErrorImagePath`) 대신 오류 및 디버그 정보가 반환됩니다.

`contents`

선택한 개체 특성을 포함하여 비네팅에서 객체 계층 구조의 XML 표현을 반환합니다. 요청의 다른 명령은 무시됩니다.

`img`

지정된 명령을 실행하고 렌더링된 이미지를 반환합니다. 응답 데이터 형식 및 응답 유형은 에 의해 결정됩니다 `fmt=`.

`imageprops`

URL 경로에 지정된 비네팅 파일 또는 카탈로그 항목의 선택된 속성을 반환합니다. 응답 [구문](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 및 응답 MIME 유형에 대한 설명은 속성을 참조하십시오. 요청의 다른 명령은 무시됩니다. 다음 속성이 반환됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>Double </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration </span> 또는 기본 실시간 시간입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>정수 </p> </td> 
   <td colname="col3"> <p>전체 해상도 높이(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>문자열 </p> </td> 
   <td colname="col3"> <p>이 비네팅과 연결된 프로필의 이름/설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>부울 </p> </td> 
   <td colname="col3"> <p>1 연결된 프로필이 비네팅에 포함된 경우 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>부울 </p> </td> 
   <td colname="col3"> <p>1 비네팅이 경로 데이터를 포함하는 경우 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>문자열 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 속성::수정자 </span> 또는 카탈로그 항목이 아닌 경우 비어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>열거형 </p> </td> 
   <td colname="col3"> <p>응답 이미지의 픽셀 유형;은 'CMYK', 'RGB' 또는 'BW'일 수 있습니다(회색 음영 이미지의 경우). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>기본 인쇄 해상도(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>문자열 </p> </td> 
   <td colname="col3"> <p>수정 날짜/시간( <span class="codeph"> 카탈로그::TimeStamp </span> 또는 비네팅 파일에서). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>정수 </p> </td> 
   <td colname="col3"> <p>전체 해상도 너비(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>문자열 </p> </td> 
   <td colname="col3"> <p>비네팅 이름(루트 비네팅 개체의 이름 문자열). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>최대 개체 해상도( <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 자재 해상도 </a> 단위(일반적으로 픽셀/인치)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>평균 개체 해상도( <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 재질 해상도 </a> 단위)입니다(일반적으로 픽셀/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 재질 해상도 </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>최소 개체 해상도( <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 재질 해상도 </a> 단위(일반적으로 픽셀/인치)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>정수 </p> </td> 
   <td colname="col3"> <p>비네팅 파일 버전 번호입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

비네팅에 포함된 이미지 맵 데이터를 반환합니다. 기본적으로 모든 가장 바깥쪽 그룹에 대한 맵 데이터가 반환됩니다. 모든 가장 안쪽 그룹에 대한 맵 데이터를

`req=map&groupLevel=-1`

맵 데이터는 크기 `wid=` 조정되거나 `hei=` 수정되지 않습니다. 응답 MIME 형식은 `<text/xml>`입니다.

응답 데이터는 HTML `<map>` 태그와 유사한 일련의 `<area>` `<AREA>` 요소가 포함된 요소로 구성됩니다.

각 `<area>` 요소에는 표준 `type=` 및 `coord=` 속성과 비네팅 그룹 이름 또는 이름 경로를 지정하는 `name=` 속성이 포함됩니다. 동일한 이름의 여러 `<area>` 요소가 해당 개체 그룹의 마스크에 비연속적인 영역이 있는 경우 나타납니다.

기본 속성 외에, 비네팅이 작성되면 추가 속성을 정의할 수 있습니다. 이러한 사용자 지정 속성은 객체 그룹 속성으로 정의됩니다. 사용자 지정 속성의 이름은 로 시작해야 합니다 `map`. 를 `<area>` 참조하십시오. 예를 들어, 그룹 속성이 포함된 `map.href=http://www.scene7.com`경우 해당 `<area>` 요소가 포함됩니다 `href="http://www.scene7.com"`.

비네팅에 맵 데이터가 포함되어 있지 않으면 빈 `<map>` 요소가 있는 XML 문서가 반환됩니다.

`object`

지정된 명령을 실행하고 남은 개체 선택(요청에서 마지막 `sel=` 또는 `obj=` 명령으로 선택한 그룹 또는 개체)으로 마스크된 렌더링된 이미지를 반환합니다. 일반적으로 알파를 지원하는 이미지 형식과 함께 사용됩니다( [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)참조). 알파를 지원하지 않는 이미지 형식을 사용하는 경우 마스크 외부 영역은 검은색입니다.

`props`

지정된 명령을 실행하고 렌더링된 이미지가 아닌 비네팅 속성과 그룹 또는 개체 속성을 반환합니다. 응답 [구문과](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 응답 MIME 유형에 대한 설명은 속성을 참조하십시오. 기본 선택 사항은 `obj=` 또는 도 지정하지 않는 한 적용됩니다(참조 `sel=` [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

응답에 다음 속성이 포함될 수 있습니다.

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
   <td> <p> 회신 이미지 배경색. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>정수 </p> </td> 
   <td> <p> 이미지 높이(픽셀 단위)를 회신합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p>ICC 프로필이 회신 이미지에 포함되면 true입니다(icc <span class="codeph"> 포함 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> = </a></span>참조). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지와 연결된 프로필의 바로 가기 이름( <span class="codeph"> icc= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"></a> </span>참조). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 응답 이미지에 알파가 포함된 경우 True입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 응답 이미지에 경로 데이터가 포함되어 있으면 true입니다( <span class="codeph"> pathEmbed <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> = </a></span>참조). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지 유형, 'CMYK', 'RGB' 또는 'BW'(회색 음영 이미지의 경우) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> 인쇄 해상도(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>정수, 부울 </p> </td> 
   <td> <p> JPEG 품질 및 크로마 플래그( <span class="codeph"> qlt= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"></a> </span>참조) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 회신 이미지의 MIME 유형입니다( <span class="codeph"><a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a></span>참조). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 이미지 너비를 픽셀 단위로 회신합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 현재 선택 항목의 속성 문자열. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 영역의 개체 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 항목의 들여쓰기 값입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 현재 선택한 개체의 전체 이름 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 영역의 오버랩 개체 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p>현재 선택 영역의 렌더링 가능한 개체 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 영역의 텍스처 가능한 개체 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 항목의 현재 표시/숨기기 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 현재 선택 영역에서 첫 번째 오버랩 객체의 Z 순서 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

의 컨텐츠를 `vignette::UserData`반환합니다. 서버에서 모든 `'??'` 항목을 줄 `vignette::UserData` `<cr><lf>`종료자()로 바꿉니다. 응답 MIME 유형이 &lt;text/plain>으로 설정된 텍스트 데이터로 답글 형식이 지정됩니다.

URL 경로에 지정된 개체가 유효한 비네팅 맵 항목으로 확인되지 않거나 비어 `vignette::UserData` `CR/LF`있는 경우 응답에 줄 종결자()만 포함됩니다.

요청 문자열의 다른 명령은 무시됩니다.

## 속성 {#section-e44092e190ff4f6380583e8ed6ea5b0b}

요청 명령. 요청 문자열의 어느 위치에서나 발생할 수 있습니다.

## 기본값 {#section-00c593cbf1af4364b6b78812e6b93c64}

URL에 이미지 경로나 수정자가 포함되어 있지 않으면 다음을 수행합니다.

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Otherwise, `req=img`

## 참조 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [속성](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
