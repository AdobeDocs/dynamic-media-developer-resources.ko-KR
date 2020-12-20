---
description: 색상 값. 16진수 표기법, 구성 요소 값의 쉼표로 구분된 목록 또는 소수 자릿수를 사용하여 색상 값을 지정할 수 있습니다.
seo-description: 색상 값. 16진수 표기법, 구성 요소 값의 쉼표로 구분된 목록 또는 소수 자릿수를 사용하여 색상 값을 지정할 수 있습니다.
seo-title: color
solution: Experience Manager
title: color
topic: Scene7 Image Serving - Image Rendering API
uuid: 61308b8e-eaac-4b2e-8500-2f9efa8a6ce8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 14%

---


# color{#color}

색상 값. 16진수 표기법, 구성 요소 값의 쉼표로 구분된 목록 또는 소수 자릿수를 사용하여 색상 값을 지정할 수 있습니다.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> gray</span>[,<span class="varname"> alpha</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>,<span class="varname"> green</span>,<span class="varname"> blue</span>[ ,<span class="varname">  </span>rgbAlpha][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>,  <span class="varname"> 자홍</span>,  <span class="varname"> 노랑</span>,  <span class="varname">  </span>검정[,알파]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 빨강</span>,  <span class="varname"> 녹색</span>,  <span class="varname"> 파랑</span>,  <span class="varname"> rgb알파</span></span> </p> </td> 
  <td class="stentry"> <p>색상 구성 요소 값(0...255, decimal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cyan</span>,  <span class="varname"> 자홍</span>,  <span class="varname"> 노란색</span>,  <span class="varname"> 검정</span>,  <span class="varname"> 알파</span></span> </p></td> 
  <td class="stentry"> <p>CMYK 색상 구성 요소 값(0.100%, 소수점) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 회색</span>,  <span class="varname"> 알파</span></span> </p> </td> 
  <td class="stentry"> <p>회색 색상 구성 요소 값(0...100%, 소수점) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>두 자리 16진수 회색 색상 값(GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>알파 색상 값(GAA)이 포함된 4자리 16진수 회색 압축 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>6자리 16진수 RGB 색상 값(RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>압축된 8자리 16진수 RRGBBA(RRGBBAA) 또는 CMYK(CCMMYYK) 색상 값('k' 접미어로 지정된 경우) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>알파 값이 포함된 10자리 16진수 CMYK(CCYYMKKAA) </p> </td> 
 </tr> 
</table>

RGB 색상의 십진수 구성 요소 값은 0...255 범위에 있습니다. CMYK 및 회색의 십진수 구성 요소 값은 0.100% 범위에 있습니다. 모든 16진수 구성 요소 값은 0...0xFF 범위에 있습니다.

색상 구성 요소 값은 미리 곱하지 않은 알파 값과 독립적인 것으로 간주됩니다.

모든 색상 값, 접두어 및 접미어는 대/소문자를 구분하지 않습니다.

CMYK 색상 값에는 문자 접미어 &#39;k&#39;가 필요합니다. RGB 및 회색 색상 값에 대해 문자 접미사를 선택적으로 지정할 수 있습니다.

16진수 회색 색상 값에 접두사 &#39;0x&#39;가 필요합니다.

&#39;s&#39; 접미사는 색상 값이 색상 값의 픽셀 유형(`attribute::IccProfileSrc*`으로 정의됨)에 해당하는 입력(소스) 색상 공간과 연결되도록 지정합니다. 이 접미어가 없으면 색상 값은 출력(대상) 색상 공간(`icc=` 또는 `attribute::IccProfile*`으로 정의)과 연결됩니다.

## 기본값 {#section-737082a7da544acca8092a48d88480e7}

알파 값을 명시적으로 지정하지 않으면 255, 0xFF 또는 100%(완전히 불투명)로 가정합니다.

## 예제 {#section-4ac69026349949f8b595a6d4a9ce474d}

유효한 색상 지정자의 일부 예 및 해당 픽셀 유형, 색상 값, 알파 값 및 기본 색상 공간의 예:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>color</i> </b> </th> 
   <th class="entry"> <b>픽셀 유형</b> </th> 
   <th class="entry"> <b>색상 값</b> </th> 
   <th class="entry"> <b>알파 값</b> </th> 
   <th class="entry"> <b>기본 색상 공간  </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255년 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0,100,200,200rs </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>200년 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255년 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160,177,194 </p> </td> 
   <td> <p>211년 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100S </p> </td> 
   <td> <p>회색 </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75g </p> </td> 
   <td> <p>회색 </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>회색 </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>회색 </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0ek </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

출력 색상의 픽셀 유형이 출력 이미지의 픽셀 유형에 해당하는 경우 `icc=`으로 지정된 출력 색상 공간이 기본 색상 공간 대신 적용됩니다.
