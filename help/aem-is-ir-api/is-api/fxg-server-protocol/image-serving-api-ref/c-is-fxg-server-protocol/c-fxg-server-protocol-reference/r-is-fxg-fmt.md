---
description: 응답 이미지 형식입니다.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 3%

---


# fmt{#fmt}

응답 이미지 형식입니다.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 클라이언트에 전송된 이미지 데이터의 이미지 인코딩 형식 및 HTTP 응답 헤더에 대한 해당 응답 MIME 형식을 지정합니다. </p> <p> <span class="codeph">  jpeg  </span>:손실 JPEG </p> <p> <span class="codeph"> png  </span>:손실 없는 PNG </p> <p> <span class="codeph"> png 알파  </span>:알파 채널이 포함된 손실 없는 PNG </p> <p> <span class="codeph">  tif  </span>:TIFF </p> <p> <span class="codeph"> tif-alpha  </span>:알파 채널이 포함된 TIFF </p> <p> <span class="codeph">  swf  </span>:Adobe swf 파일에 포함된 손실 JPEG </p> <p> <span class="codeph"> pdf  </span>:PDF에 포함된 이미지 </p> <p> <span class="codeph"> gif  </span>:2~256색 GIF </p> <p> <span class="codeph"> gif-alpha  </span>:2~255색 및 키 색상 투명도가 포함된 GIF </p> <p> <span class="codeph"> fxg  </span>:변수 및 DOM 조작이 적용된 FXG </p> <p> <span class="codeph">  fxgraw  </span>:서버에 저장된 원본 FXG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | 회색 | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 출력 색상 공간에 효과를 적용할 수 있습니다. </p> <p> <span class="codeph">  rgb  </span>:RGB 이미지 데이터 반환 </p> <p> <span class="codeph"> 회색  </span>:회색 비율 이미지 데이터 반환 </p> <p> <span class="codeph"> cmyk  </span>:CMYK 이미지 데이터 반환 </p> </td> 
 </tr> 
</table>

`tiffCompression` 은 tif-alpha가 형식으로 지정된 경우에만 허용됩니다. 이러한 이미지 형식에 대해 지원되는 압축 옵션은 아래 표를 참조하십시오.

`qlt=` 다음과 같은 형식의 JPEG 인코딩 옵션을 설정하는 데 사용할 수 있습니다.JPEG, JPEG 압축 TIFF. quanze=는 fmt=gif 또는 fmt=gif-alpha일 경우 사용할 수 있습니다. 자세한 내용은 명령 설명을 참조하십시오. 다른 형식에는 설정 가능한 옵션이 없습니다.

모든 형식 및 `pixelTypes[7]`에 대해 픽셀 구성 요소당 8비트가 반환됩니다.

다음 표에는 해당 HTTP 응답 MIME 유형인 `pixelType` 형식과 형식의 유효한 조합이 나열되어 있습니다.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> 형식</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>응답 MIME 유형 </p> </th> 
   <th colname="col4" class="entry"> <p>ICC 프로필 포함 </p> </th> 
   <th colname="col5" class="entry"> <p>옵션 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, 회색, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb, 회색 </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, 회색, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( 없음) | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, 회색, cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>예 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb, 회색 </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>아니오 </p> </td> 
   <td> <p><span class="codeph"> 수량화=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
