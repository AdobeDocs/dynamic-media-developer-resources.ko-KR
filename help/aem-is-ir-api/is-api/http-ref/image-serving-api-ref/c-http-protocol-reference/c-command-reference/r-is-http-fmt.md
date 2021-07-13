---
description: 응답 이미지 형식입니다.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 5%

---

# fmt{#fmt}

응답 이미지 형식입니다.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | jpeg | jpeg2000-알파 | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | 설명 |
|---|---|
| `avif-alpha` | 알파 채널이 있는 손실 및 무손실 AVIF <br><br>*이 형식의 릴리스 타임라인:* <br><b>북미</b> - 지금 사용 가능<br><b>유럽, 중동, 아프리카</b> - 2021년 8월 13일<br><b>아시아-태평양</b> - 지금 사용 가능 |
| `avif` | 손실 및 무손실 AVIF <br><br>*이 형식의 릴리스 타임라인:*<br><b>&#x200B;북아메리카</b> - 지금 사용 가능<br><b>유럽, 중동, 아프리카</b> - 2021년 8월 13일<br><b>아시아-태평양</b> - 지금 사용 가능 |
| `eps` | 압축되지 않은 이진 캡슐화된 PostScript |
| `f4m` | Flash 스트리밍 서버 매니페스트 형식 |
| `gif-alpha` | 2-256개 색상과 주요 색상 투명도가 있는 GIF |
| `gif` | 2~256색 GIF |
| `jpeg` | 손실 JPEG |
| `jpeg2000-alpha` | 알파 채널 포함 손실 및 손실 없는 JPEG 2000 |
| `jpeg2000` | 손실 및 손실 없는 JPEG 2000 |
| `jpegxr-alpha` | 알파 채널이 있는 손실 및 손실 없는 JPEG XR |
| `jpegxr` | 손실 및 손실 없는 JPEG XR |
| `jpg` | 손실 JPG |
| `m3u8` | Apple 스트리밍 서버 매니페스트 형식 |
| `pdf` | PDF에 포함된 이미지 |
| `pjpeg` | 프로그레시브 JPEG |
| `png-alpha` | 알파 채널이 있는 24비트 무손실 PNG |
| `png` | 24비트 무손실 PNG |
| `png8-alpha` | 알파 채널이 있는 8비트 무손실 PNG |
| `png8` | 8비트 무손실 PNG |
| `swf-alpha` | Adobe AS2 swf 파일에 포함된 손실 JPEG 및 디플레이트 압축 마스크 |
| `swf` | Adobe AS2 swf 파일에 포함된 손실 JPEG |
| `swf3-alpha` | Adobe AS3 swf 파일에 포함된 JPEG와 디플레이트 압축 마스크의 손실. **참고:** swf 및 swf-알파 형식은 ActionScript 2 응용 프로그램(Flash Player 8 이하)에 가장 잘 사용됩니다. ActionScript3 응용 프로그램(Flash Player 9 이상)에는 swf3 및 swf3-alpha 형식을 사용하는 것이 좋습니다 |
| `swf3` | Adobe AS3 swf 파일에 포함된 손실 JPEG |
| `tif-alpha` | 알파 채널이 있는 TIFF |
| `tif` | TIFF |
| `webp-alpha` | 알파 채널이 있는 손실 및 손실 없는 WebP |
| `webp` | 손실 및 손실 없는 WebP |

| *`pixelType`* – rgb | 회색 | cmyk |
| *`pixelType`* | 설명 |
|---|---|
| `cmyk` | CMYK 이미지 데이터를 반환합니다. |
| `gray` | 회색 음영 이미지 데이터를 반환합니다. |
| `rgb` | RGB 이미지 데이터를 반환합니다. |

| *`compression`* – none | lzw | zip | jpeg | 손실 | 무손실 |
| *`compression`* | 설명 |
|---|---|
| `jpeg` | JPEG 압축(손실) |
| `lossy` | WebP, JPEG 2000 및 JPEG XR 압축(손실) |
| `lossless` | WebP, JPEG 2000 및 JPEG XR 압축(무손실) |
| `lzw` | LZW(Lempel-Ziv-Welch) 압축(손실 없음) |
| `none` | 압축 해제됨 |
| `zip` | &quot;Deflate&quot; 압축(손실 없음) |

* *`format`* 클라이언트로 전송되는 이미지 데이터의 이미지 인코딩 형식과 HTTP 응답 헤더에 대한 해당 응답 MIME 유형을 지정합니다.
* *`pixelType`* 을 지정하지 않은 경우 출력 색상 공간 변환 `icc=` 을 적용하는 데 사용할 수 있습니다.

   *`pixelType`*&#x200B;에 해당하는 기본 색상 프로필이 적용됩니다. 색상 관리를 사용하지 않도록 설정하면 자동 전환이 적용됩니다. *`pixelType`* 이 지정되면 이  `icc=` 무시됩니다. 이 값은 출력 픽셀 유형을 결정합니다.

* *`compression`* 는  `tif`,  `tif-alpha`,  `pdf`,  `webp`,  `webp-alpha`,  `jpeg2000`,  `jpeg2000-alpha`,  `jpegxr` 또는  `jpegxr-alpha` 가  *`format`*&#x200B;로 지정된 경우에만 허용됩니다. 이러한 이미지 형식에 대해 지원되는 압축 옵션에 대해서는 아래 표를 참조하십시오.

`qlt=` 을 사용하여 다음 형식에 대한 JPEG 인코딩 옵션을 설정할 수 있습니다. JPEG, JPEG 압축으로 TIFF, JPEG 압축으로 PDF, SWF WebP, JPEG 2000 및 JPEG XR도 `qlt=`을 사용하지만, 이 값은 다른 형식의 품질에 대해 다른 특성을 갖게 됩니다. `fmt=gif` 또는 `fmt=gif-alpha`인 경우 `quantize=`을 사용하십시오. 자세한 내용은 명령 설명을 참조하십시오. 다른 형식에는 설정 가능한 옵션이 없습니다.

모든 *`formats`* 및 *`pixelTypes`*(GIF의 경우 픽셀당 8비트)에 대해 픽셀 구성 요소당 8비트가 반환됩니다.

다음 표에는 *`format`*와 *`pixelType`* 의 유효한 조합, 해당 HTTP 응답 MIME 유형, ICC 프로필을 포함할 수 있는지 여부([iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e) 참조) 및 적용할 수 있는 형식별 옵션이 나와 있습니다.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 포맷</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> 응답 MIME 유형</b> </th> 
   <th class="entry"> <b>포함 ICC 프로필</b> </th> 
   <th class="entry"> <b> 옵션</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>,  <span class="codeph"> pscan=  </span>,  <span class="codeph"> qlt=  </span>,  <span class="codeph"> xmpEmbed=  </span> </p> <p><span class="codeph"> pscan= </span> 매개 변수는 pjpeg 형식에만 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-알파 </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-알파 </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 압축  </span> </span> <p> ( <span class="codeph"> 없음|lzw|zip|jpeg </span>) </p> <p>'tiff'만 'tiff-alpha'는 jpeg 압축을 지원하지 않습니다. </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> qlt=  </span> 압축이  <span class="varname"> jpeg </span> 로 설정되어 있지 않으면  <span class="codeph"> 무시됩니다  </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>아니요 </p> <p> <p>참고:  Adobe Flash Player은 포함된 ICC 프로파일을 무시합니다. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> 특성::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 압축  </span> </span> <p> ( <span class="codeph"> 없음|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt=  </span> 압축이  <span class="codeph"> <span class="varname"> jpeg </span> </span> 로 설정되어 있지 않으면  <span class="codeph"> 무시됩니다  </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> <p>데이터는 회색 또는 rgb로 변환된 후 팔레트로 변환됩니다. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>아니요 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> 정량=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>아니요 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 압축  </span> </span> ( <span class="codeph"> 손실  </span>,  <span class="codeph"> 손실  </span>없음) </p> <p> <span class="codeph"> 무손실 </span> 에 대해서는 qlt=  <span class="codeph"> 가 무시됩니다  </span>. </p> <p>WebP 형식에는 색차 다운샘플링이라는 개념이 없으므로 <span class="codeph"> qlt </span>(예: <span class="codeph"> qlt=80,1 </span>)와 함께 두 번째 값을 사용하는 경우(예: <span class="codeph"> 1 </span>)는 무시됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-알파 </p> </td> 
   <td> <p>rgb, 회색 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>아니요 </p> </td> 
   <td> <p>위와 같습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>아니요 </p> </td> 
   <td> <p>위와 같습니다. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>아니요 </p> </td> 
   <td> <p>위와 같습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

요청 속성입니다. `req=img`(기본값) 또는 `req=mask`; 인 경우 현재 레이어 설정에 관계없이 적용됩니다. 그렇지 않으면 무시됩니다.

*`type`* 이 지정된 경우  `iccProfile=` 가 무시됩니다.

## 기본값 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`으로, 여기서  *`defaultType`* 는 다음과 같이 처리됩니다. 지정한  `icc=` 경우, 은  *`defaultType`* 지정된 ICC 프로파일의 픽셀 유형에 해당합니다. `icc=`이 지정되지 않은 경우 *`defaultType`*&#x200B;은 `gray`이고, `req=mask`이면 `rgb`입니다.

## 예제 {#section-b93222e652df404a84c69025247f07df}

**JPEG 형식으로 작은 품질의 미리 보기 이미지를 요청합니다(기본값).**

` http:// *`서버`*/myRootId/myImageId?qlt=60&wid=200`

**회색으로 변환된 동일한 이미지를 요청합니다.**

` http:// *`서버`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**알파 채널과 고해상도로 손실 없는 형식으로 동일한 이미지를 요청합니다.**

` http:// *`서버`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**회색 음영 TIFF 이미지와 동일한 이미지에 대한 알파 채널을 요청합니다.**

` http:// *`서버`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**기본 ICC 프로파일을 사용하여 동일한 이미지를 cmyk로 변환합니다.**

` http:// *`서버`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**다른 ICC 프로파일을 사용하여 동일한 이미지를 cmyk로 변환하고 TIFF 이미지에 프로파일을 포함합니다.**

` http:// *`서버`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**이 이미지를 픽셀 유형 변환 없이 JPEG 압축으로 TIF 파일로 전달합니다.**

` http:// *`서버`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**키 색상 투명도와 힘 색상을 흑백으로 사용하여 이미지를 두 가지 색조 GIF로 변환합니다.**

` http:// *`서버`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**품질 설정이 80인 손실:**

` http:// *`서버`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**알파 포함 무손실:**

` http:// *`서버`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**품질 설정이 80인 손실:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**알파 포함 무손실:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**품질 설정이 80인 손실:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**알파 포함 무손실:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 참조 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301),  [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
