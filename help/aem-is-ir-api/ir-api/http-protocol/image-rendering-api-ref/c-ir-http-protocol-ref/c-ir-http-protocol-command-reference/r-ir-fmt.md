---
description: 응답 이미지 형식. 클라이언트에 전송된 이미지 데이터의 이미지 인코딩 형식 및 HTTP 응답 헤더에 대한 해당 응답 MIME 형식을 지정합니다.
seo-description: 응답 이미지 형식. 클라이언트에 전송된 이미지 데이터의 이미지 인코딩 형식 및 HTTP 응답 헤더에 대한 해당 응답 MIME 형식을 지정합니다.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c589119-d1b3-460f-acbd-5e8d10d0d976
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# fmt{#fmt}

응답 이미지 형식. 클라이언트에 전송된 이미지 데이터의 이미지 인코딩 형식 및 HTTP 응답 헤더에 대한 해당 응답 MIME 형식을 지정합니다.

` fmt= *``*[,[ *``*][, *`formatpixelTypeffCompression`*`]

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 형식 </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>손실 있는 JPEG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>손실 JPG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>손실 없는 PNG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>알파 채널이 포함된 손실 없는 PNG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>알파 채널이 포함된 TIFF </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>Macromedia swf 파일에 임베드된 손실 JPEG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>Macromedia swf 파일에 임베드된 손실 JPEG 및 압축 마스크입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>PDF에 포함된 이미지 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>압축되지 않은 바이너리 캡슐화된 PostScript. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>256색 GIF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>255색 및 키 색상 투명도가 포함된 GIF </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>RGB 이미지 데이터를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>회색 </p> </td> 
  <td class="stentry"> <p>회색 음영 이미지 데이터를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>CMYK 이미지 데이터를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>없음 </p> </td> 
  <td class="stentry"> <p>압축 해제됨. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW(Lempel-Ziv-Welch) 압축(손실 없음) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>"Deflate" 압축(손실 없음). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG 압축(손실). </p> </td> 
 </tr> 
</table>

*`pixelType`* 지정하지 `icc=` 않은 경우 효과 출력 색상 공간 변환에 해당하는 기본 색상 프로필이 *`pixelType`* 적용됩니다. 색상 관리가 비활성화되면 자동 변환이 적용됩니다. *`pixelType`* 가 지정된 경우 무시되며, `icc=` 이 경우 출력 픽셀 유형이 결정됩니다.

*`compression`* 은 tif, tif-alpha 또는 PDF가 *`format`*&#x200B;로 지정된 경우에만 허용됩니다. 이러한 이미지 형식에 대해 지원되는 압축 옵션은 아래 표를 참조하십시오.

`qlt-` 다음과 같은 형식의 JPEG 인코딩 옵션을 설정합니다.JPEG, JPEG 압축 TIFF, JPEG 압축 PDF 및 SWF 파일 if `quantize=` or `fmt=gif` 을 `fmt=gif-alpha`사용하십시오. 자세한 내용은 명령 설명을 참조하십시오. 다른 형식에는 설정 가능한 옵션이 없습니다.

픽셀 구성 요소당 8비트는 모든 포맷 및 픽셀 유형에 대해 반환됩니다.

다음 표에는 ICC 프로필을 포함할 수 있는지 여부(iccEmbed= *`format`* 참조) *`pixelType`*&#x200B;및 [해당 HTTP 응답 MIME 유형의 유효한 조합과 적용할 수 있는](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)형식별 옵션 명령이 나와 있습니다.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> 형식 </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType </span> </p> </th> 
   <th colname="col3" class="entry"> <p>응답 MIME 유형 </p> </th> 
   <th colname="col4" class="entry"> <p>ICC 프로필 포함 </p> </th> 
   <th colname="col5" class="entry"> <p>옵션 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif, alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt </span> </p> <p>( <span class="codeph"> qlt= </span> 는 tiff <span class="varname"> Compression이 'jpeg' </span> 로 설정되어 있지 않으면 무시됩니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>아니요 </p> <p>Flash Player는 포함된 ICC 프로필을 무시합니다. </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (없음|zip|jpeg),qlt= </span> </p> <p> ( <span class="codeph"> qlt= </span> 는 tiff <span class="varname"> Compression이 'jpeg' </span> 로 설정되어 있지 않으면 무시됩니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> <p>(데이터는 회색 또는 rgb로 변환 후 팔레트로 변환됩니다.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>아니요 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

클라이언트에 전송된 응답 이미지 데이터의 인코딩 형식 및 HTTP 응답 헤더에 대한 해당 응답 MIME 형식을 지정합니다.

`png-alpha` 연결되지 않은 알파(즉, 알파는 픽셀 값에 미리 곱하지 않음)를 반환하고 관련 알파 `tif-alpha`값을 `swf-alpha` 반환합니다. 즉, 알파 값은 알파 값과 미리 곱해집니다. 알파 채널은 비네팅의 배경 마스크의 반대와 `req=img`경우에 해당하는 그룹 또는 개체 마스크에 해당합니다 `req=object`. 중첩된 IR 요청을 사용할 때 알파를 적용하려면 포함된 IR 요청 및 기본 요청에 적절한 알파 파일 `fmt=` 형식과 함께 추가합니다. CMYK 또는 회색 음영 ICC 프로파일이 로 지정된 경우 알파 데이터가 반환되지 `icc=`않습니다.

## 속성 {#section-eb12a82c69d84622bcea153dd84d95b3}

요청에서 어느 곳에서나 발생할 수 있습니다.

## 기본값 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* 의 기본값은 `attribute::Format`로 설정되어 있고 *`tiffCompression`* 기본값은 `attribute::TiffEncoding`로 설정되어 있습니다. *`pixelType`* 가 지정되지 `rgb` 않은 `icc=` 경우 기본값을 지정하고, 그렇지 않은 경우 지정된 ICC 프로필의 픽셀 유형에 해당합니다.

## 참조 {#section-c55efc881fc94c70bff91b870e026a7b}

[속성::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [속성::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [속성::TiffLt=](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e), iccEmbed= [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)[, qembed=embed, pathEmbed=Path, Represq=qualze=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
